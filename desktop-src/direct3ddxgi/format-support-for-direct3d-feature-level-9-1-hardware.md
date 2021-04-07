---
description: Cette section spécifie les formats ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valeurs) qui sont pris en charge dans la fonctionnalité Direct3D 10Level9 le matériel 9,1.
ms.assetid: 770A5396-C5D9-442B-99FE-3D220C54E8EB
title: Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 9.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56653fd2fb504e3f23cfac13b432530ebaa7219b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846042"
---
# <a name="format-support-for-direct3d-feature-10level9-91-hardware"></a><span data-ttu-id="fbb75-103">Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 9.1</span><span class="sxs-lookup"><span data-stu-id="fbb75-103">Format support for Direct3D Feature 10Level9 9.1 hardware</span></span>

<span data-ttu-id="fbb75-104">Cette section spécifie les formats ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valeurs) qui sont pris en charge dans la fonctionnalité Direct3D 10Level9 9,1 Hardware.</span><span class="sxs-lookup"><span data-stu-id="fbb75-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.1 hardware.</span></span>

<span data-ttu-id="fbb75-105">Le tableau récapitule la prise en charge des fonctionnalités à l’aide de la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="fbb75-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="fbb75-106">Symbole</span><span class="sxs-lookup"><span data-stu-id="fbb75-106">Symbol</span></span>                            | <span data-ttu-id="fbb75-107">Description</span><span class="sxs-lookup"><span data-stu-id="fbb75-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="fbb75-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="fbb75-108">_ *-*\*</span></span>                             | <span data-ttu-id="fbb75-109">Non autorisé ou non disponible.</span><span class="sxs-lookup"><span data-stu-id="fbb75-109">Disallowed or not available.</span></span>                                                  |
| ![obligatoire](images/letter-r.jpg)  | <span data-ttu-id="fbb75-111">Un support matériel est requis.</span><span class="sxs-lookup"><span data-stu-id="fbb75-111">Hardware support is required.</span></span>                                                 |
| ![facultatif](images/letter-o.jpg)  | <span data-ttu-id="fbb75-113">Prise en charge du matériel facultative, le format peut ou non être accéléré par le matériel.</span><span class="sxs-lookup"><span data-stu-id="fbb75-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dépendants](images/letter-d.jpg) | <span data-ttu-id="fbb75-115">Obligatoire si la fonctionnalité facultative associée est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fbb75-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="fbb75-116">Cette rubrique contient une section par format.</span><span class="sxs-lookup"><span data-stu-id="fbb75-116">This topic contains a section per format.</span></span> <span data-ttu-id="fbb75-117">Une *cible* de format (tables contenant une ligne par cible) peut être un type de ressource, une fonction intrinsèque HLSL ou une fonctionnalité particulière qui est dépendante d’un format particulier.</span><span class="sxs-lookup"><span data-stu-id="fbb75-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="fbb75-118">Pour vérifier par programmation la prise en charge du format dans D3D11 et D3D12, consultez vérification de la [prise en charge des fonctionnalités matérielles](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="fbb75-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="fbb75-119">Les nombres des formats sont principalement, mais pas tous, dans l’ordre numérique croissant, &mdash; certains ne sont pas triés par ordre numérique et sont répertoriés avec d’autres formats pertinents.</span><span class="sxs-lookup"><span data-stu-id="fbb75-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="fbb75-120">Notez également que les *types* sans type dans un nom de format peuvent signifier un type *partiellement* typé, et non strictement typés (reportez-vous à la section Remarques sur le [format](#format-notes) à la fin de la rubrique).</span><span class="sxs-lookup"><span data-stu-id="fbb75-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

// 

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="fbb75-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="fbb75-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="fbb75-122">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-122">Target</span></span> | <span data-ttu-id="fbb75-123">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-123">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-124">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-125">0</span><span class="sxs-lookup"><span data-stu-id="fbb75-125">0</span></span> |
| <span data-ttu-id="fbb75-126">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-126">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-127">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-128">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-129">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-130">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-131">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-132">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-133">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-134">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-135">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-136">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-137">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-138">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-139">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-140">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-141">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-141">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-142">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-144">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-145">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-146">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-147">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-148">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-149">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-150">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-151">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-152">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-153">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-155">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-156">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-157">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-158">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-159">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-160">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-161">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-162">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-163">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-164">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-165">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-166">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-167">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-168">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-169">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-170">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="fbb75-171">\_<sup>PC</sup> DXGI_FORMAT_R32G32B32A32 type (1)</span><span class="sxs-lookup"><span data-stu-id="fbb75-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="fbb75-172">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-172">Target</span></span> | <span data-ttu-id="fbb75-173">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-173">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-174">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-175">128</span><span class="sxs-lookup"><span data-stu-id="fbb75-175">128</span></span> |
| <span data-ttu-id="fbb75-176">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-176">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-177">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-178">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-179">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-180">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-181">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-182">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-183">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-184">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-185">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-186">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-187">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-188">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-189">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-190">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-191">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-191">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-192">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-194">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-195">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-196">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-197">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-198">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-199">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-200">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-201">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-202">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-203">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-205">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-206">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-207">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-208">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-209">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-210">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-211">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-212">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-213">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-214">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-215">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-216">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-217">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-218">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-219">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-220">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="fbb75-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FNS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="fbb75-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="fbb75-222">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-222">Target</span></span> | <span data-ttu-id="fbb75-223">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-223">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-224">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-225">128</span><span class="sxs-lookup"><span data-stu-id="fbb75-225">128</span></span> |
| <span data-ttu-id="fbb75-226">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-226">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-228">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-229">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-229">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-231">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-232">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-233">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-234">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-235">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-235">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-236">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-236">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-237">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-237">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-238">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-238">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-239">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-239">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-240">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-240">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-241">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-241">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-242">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-242">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-243">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-243">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-244">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-244">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-245">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-245">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-246">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-246">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-247">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-247">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-248">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-248">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-249">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-249">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-250">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-250">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-251">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-251">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-252">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-252">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-253">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-253">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-254">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-254">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-255">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-255">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-256">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-256">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-257">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-257">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-258">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-258">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-259">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-259">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-260">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-260">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-261">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-261">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-262">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-262">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-263">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-263">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-264">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-264">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-265">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-265">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-266">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-266">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-267">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-267">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-268">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-268">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-269">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-269">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-270">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-270">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-271">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-271">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-272">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-272">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="fbb75-273">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FNS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="fbb75-273">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="fbb75-274">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-274">Target</span></span> | <span data-ttu-id="fbb75-275">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-275">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-276">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-276">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-277">128</span><span class="sxs-lookup"><span data-stu-id="fbb75-277">128</span></span> |
| <span data-ttu-id="fbb75-278">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-278">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-279">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-279">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-280">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-281">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-282">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-283">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-284">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-285">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-286">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-287">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-287">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-288">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-288">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-289">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-289">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-290">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-290">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-291">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-291">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-292">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-292">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-293">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-293">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-294">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-294">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-295">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-295">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-296">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-296">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-297">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-297">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-298">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-298">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-299">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-299">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-300">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-300">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-301">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-301">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-302">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-302">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-303">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-303">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-304">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-304">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-305">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-305">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-306">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-306">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-307">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-307">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-308">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-308">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-309">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-309">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-310">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-310">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-311">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-311">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-312">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-312">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-313">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-313">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-314">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-314">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-315">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-315">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-316">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-316">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-317">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-317">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-318">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-318">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-319">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-319">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-320">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-320">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-321">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-321">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-322">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-322">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="fbb75-323">DXGI_FORMAT_R32G32B32A32 \_ Saint<sup>FNS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="fbb75-323">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="fbb75-324">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-324">Target</span></span> | <span data-ttu-id="fbb75-325">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-325">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-326">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-326">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-327">128</span><span class="sxs-lookup"><span data-stu-id="fbb75-327">128</span></span> |
| <span data-ttu-id="fbb75-328">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-328">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-329">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-329">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-330">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-330">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-331">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-332">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-333">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-334">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-335">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-335">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-336">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-337">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-337">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-338">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-338">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-339">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-339">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-340">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-340">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-341">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-341">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-342">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-342">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-343">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-343">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-344">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-345">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-346">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-347">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-348">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-349">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-350">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-351">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-351">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-352">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-353">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-354">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-355">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-356">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-357">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-358">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-359">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-360">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-360">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-361">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-361">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-362">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-362">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-363">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-363">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-364">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-364">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-365">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-365">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-366">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-366">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-367">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-367">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-368">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-369">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-370">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-371">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-371">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-372">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="fbb75-373">\_<sup>PC</sup> DXGI_FORMAT_R32G32B32 type (5)</span><span class="sxs-lookup"><span data-stu-id="fbb75-373">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="fbb75-374">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-374">Target</span></span> | <span data-ttu-id="fbb75-375">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-375">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-376">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-377">96</span><span class="sxs-lookup"><span data-stu-id="fbb75-377">96</span></span> |
| <span data-ttu-id="fbb75-378">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-378">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-379">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-379">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-380">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-381">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-382">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-383">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-384">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-385">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-385">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-386">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-387">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-387">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-388">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-388">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-389">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-389">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-390">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-390">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-391">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-391">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-392">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-392">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-393">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-393">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-394">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-394">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-395">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-395">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-396">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-396">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-397">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-398">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-399">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-400">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-401">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-401">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-402">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-403">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-404">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-405">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-406">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-407">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-408">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-408">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-409">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-409">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-410">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-410">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-411">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-411">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-412">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-412">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-413">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-413">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-414">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-414">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-415">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-415">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-416">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-416">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-417">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-417">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-418">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-418">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-419">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-419">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-420">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-420">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-421">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-421">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-422">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="fbb75-423">DXGI_FORMAT_R32G32B32 \_ float<sup>FNS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="fbb75-423">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="fbb75-424">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-424">Target</span></span> | <span data-ttu-id="fbb75-425">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-425">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-426">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-427">96</span><span class="sxs-lookup"><span data-stu-id="fbb75-427">96</span></span> |
| <span data-ttu-id="fbb75-428">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-428">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-430">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-430">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-431">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-431">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-433">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-433">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-434">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-434">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-435">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-435">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-436">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-436">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-437">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-438">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-439">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-440">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-441">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-442">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-443">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-443">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-444">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-445">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-445">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-446">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-447">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-448">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-448">Blendable RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="fbb75-450">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-450">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-451">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-451">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-452">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-452">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-453">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-453">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-454">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-454">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-455">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-455">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-456">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-456">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-457">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-457">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-458">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-458">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-459">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-459">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-460">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-460">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-461">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-461">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-462">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-462">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-463">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-463">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-464">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-464">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="fbb75-466">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-466">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="fbb75-468">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-468">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-469">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-469">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-470">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-470">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-471">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-471">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-472">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-472">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-473">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-473">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-474">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-474">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-475">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-475">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-476">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-476">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-477">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-477">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="fbb75-478">DXGI_FORMAT_R32G32B32 \_ uint<sup>FNS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="fbb75-478">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="fbb75-479">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-479">Target</span></span> | <span data-ttu-id="fbb75-480">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-480">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-481">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-481">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-482">96</span><span class="sxs-lookup"><span data-stu-id="fbb75-482">96</span></span> |
| <span data-ttu-id="fbb75-483">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-483">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-484">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-484">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-485">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-485">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-486">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-486">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-487">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-487">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-488">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-488">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-489">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-489">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-490">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-491">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-491">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-492">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-492">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-493">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-493">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-494">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-494">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-495">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-495">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-496">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-496">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-497">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-497">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-498">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-498">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-499">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-499">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-500">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-500">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-501">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-501">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-502">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-502">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-503">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-503">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-504">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-504">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-505">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-505">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-506">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-506">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-507">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-507">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-508">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-508">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-509">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-509">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-510">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-510">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-511">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-511">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-512">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-512">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-513">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-513">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-514">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-514">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-515">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-515">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-516">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-516">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="fbb75-518">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-518">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="fbb75-520">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-520">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-521">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-521">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-522">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-522">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-523">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-523">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-524">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-524">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-525">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-526">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-527">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-528">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-528">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-529">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-529">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="fbb75-530">DXGI_FORMAT_R32G32B32 \_ Saint<sup>FNS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="fbb75-530">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="fbb75-531">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-531">Target</span></span> | <span data-ttu-id="fbb75-532">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-532">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-533">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-533">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-534">96</span><span class="sxs-lookup"><span data-stu-id="fbb75-534">96</span></span> |
| <span data-ttu-id="fbb75-535">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-535">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-536">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-536">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-537">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-537">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-538">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-539">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-540">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-541">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-541">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-542">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-542">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-543">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-544">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-544">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-545">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-545">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-546">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-546">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-547">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-547">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-548">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-548">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-549">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-549">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-550">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-550">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-551">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-551">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-552">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-552">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-553">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-553">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-554">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-554">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-555">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-555">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-556">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-556">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-557">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-557">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-558">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-558">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-559">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-559">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-560">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-560">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-561">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-561">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-562">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-562">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-563">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-563">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-564">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-564">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-565">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-565">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-566">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-566">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-567">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-567">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-568">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-568">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="fbb75-570">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-570">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="fbb75-572">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-572">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-573">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-573">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-574">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-574">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-575">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-575">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-576">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-576">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-577">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-577">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-578">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-578">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-579">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-579">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-580">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-580">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-581">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-581">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="fbb75-582">\_<sup>PC</sup> DXGI_FORMAT_R16G16B16A16 type (9)</span><span class="sxs-lookup"><span data-stu-id="fbb75-582">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="fbb75-583">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-583">Target</span></span> | <span data-ttu-id="fbb75-584">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-584">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-585">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-585">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-586">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-586">64</span></span> |
| <span data-ttu-id="fbb75-587">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-587">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-588">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-588">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-589">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-589">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-590">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-590">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-591">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-591">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-592">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-592">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-593">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-593">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-594">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-594">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-595">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-595">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-596">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-596">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-597">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-597">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-598">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-598">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-599">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-599">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-600">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-600">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-601">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-601">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-602">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-602">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-603">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-603">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-604">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-604">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-605">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-606">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-606">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-607">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-607">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-608">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-608">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-609">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-609">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-610">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-610">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-611">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-611">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-612">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-612">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-613">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-613">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-614">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-614">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-615">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-615">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-616">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-616">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-617">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-617">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-618">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-618">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-619">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-619">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-620">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-620">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-621">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-621">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-622">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-622">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-623">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-623">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-624">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-624">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-625">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-625">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-626">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-626">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-627">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-627">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-628">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-628">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-629">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-629">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-630">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-630">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-631">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-631">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="fbb75-632">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FNS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="fbb75-632">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="fbb75-633">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-633">Target</span></span> | <span data-ttu-id="fbb75-634">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-634">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-635">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-635">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-636">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-636">64</span></span> |
| <span data-ttu-id="fbb75-637">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-637">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-638">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-638">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-639">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-639">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-640">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-640">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-641">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-641">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-642">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-642">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-643">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-643">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-644">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-644">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-645">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-645">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-646">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-646">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-647">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-647">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-648">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-649">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-650">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-650">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-651">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-652">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-652">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-653">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-653">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-654">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-654">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-655">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-655">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-656">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-656">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-657">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-657">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-658">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-658">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-659">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-659">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-660">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-660">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-661">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-661">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-662">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-662">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-663">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-663">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-664">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-664">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-665">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-665">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-666">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-666">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-667">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-667">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-668">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-668">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-669">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-669">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-670">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-670">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-671">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-671">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-672">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-672">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-673">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-673">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-674">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-674">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-675">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-675">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-676">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-676">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-677">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-677">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-678">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-678">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-679">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-680">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-680">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-682">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="fbb75-683">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="fbb75-683">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="fbb75-684">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-684">Target</span></span> | <span data-ttu-id="fbb75-685">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-685">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-686">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-687">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-687">64</span></span> |
| <span data-ttu-id="fbb75-688">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-688">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-689">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-689">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-690">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-690">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-691">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-691">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-692">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-692">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-693">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-693">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-694">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-695">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-696">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-696">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-697">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-697">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-698">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-698">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-699">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-700">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-701">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-701">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-702">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-703">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-703">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-704">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-704">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-705">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-705">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-706">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-706">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-707">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-707">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-708">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-708">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-709">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-709">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-710">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-710">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-711">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-711">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-712">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-712">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-713">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-713">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-714">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-714">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-715">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-715">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-716">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-716">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-717">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-717">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-718">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-718">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-719">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-719">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-720">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-720">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-721">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-721">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-722">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-722">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-723">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-723">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-724">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-724">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-725">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-725">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-726">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-726">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-727">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-727">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-728">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-728">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-729">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-729">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-730">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-730">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-731">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-731">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-732">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-732">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="fbb75-733">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="fbb75-733">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="fbb75-734">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-734">Target</span></span> | <span data-ttu-id="fbb75-735">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-735">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-736">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-736">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-737">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-737">64</span></span> |
| <span data-ttu-id="fbb75-738">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-738">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-739">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-740">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-741">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-742">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-743">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-744">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-744">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-745">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-745">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-746">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-746">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-747">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-747">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-748">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-748">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-749">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-749">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-750">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-750">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-751">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-751">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-752">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-752">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-753">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-753">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-754">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-754">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-755">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-755">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-756">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-756">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-757">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-757">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-758">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-758">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-759">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-759">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-760">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-760">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-761">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-761">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-762">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-762">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-763">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-763">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-764">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-764">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-765">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-765">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-766">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-766">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-767">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-767">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-768">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-768">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-769">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-769">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-770">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-770">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-771">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-771">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-772">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-772">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-773">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-773">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-774">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-774">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-775">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-775">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-776">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-776">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-777">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-777">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-778">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-778">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-779">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-779">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-780">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-780">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-781">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-781">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-782">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="fbb75-783">DXGI_FORMAT_R16G16B16A16 \_ ronfler<sup>FNS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="fbb75-783">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="fbb75-784">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-784">Target</span></span> | <span data-ttu-id="fbb75-785">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-785">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-786">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-787">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-787">64</span></span> |
| <span data-ttu-id="fbb75-788">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-788">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-790">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-790">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-791">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-791">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-793">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-793">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-794">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-794">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-795">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-795">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-796">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-796">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-797">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-798">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-799">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-799">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-800">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-800">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-801">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-801">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-802">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-802">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-803">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-803">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-804">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-804">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-805">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-805">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-806">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-807">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-808">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-809">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-810">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-811">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-812">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-813">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-813">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-814">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-815">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-816">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-817">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-818">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-819">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-820">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-821">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-822">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-822">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-823">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-823">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-824">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-824">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-825">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-825">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-826">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-826">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-827">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-827">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-828">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-828">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-829">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-829">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-830">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-830">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-831">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-831">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-832">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-832">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-833">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-833">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-834">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-834">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="fbb75-835">DXGI_FORMAT_R16G16B16A16 \_ Saint<sup>FNS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="fbb75-835">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="fbb75-836">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-836">Target</span></span> | <span data-ttu-id="fbb75-837">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-837">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-838">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-838">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-839">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-839">64</span></span> |
| <span data-ttu-id="fbb75-840">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-840">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-842">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-842">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-843">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-843">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-845">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-845">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-846">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-846">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-847">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-847">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-848">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-848">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-849">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-849">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-850">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-850">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-851">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-851">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-852">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-852">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-853">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-853">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-854">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-854">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-855">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-855">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-856">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-856">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-857">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-857">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-858">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-858">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-859">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-859">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-860">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-860">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-861">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-861">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-862">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-862">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-863">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-863">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-864">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-864">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-865">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-865">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-866">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-866">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-867">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-867">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-868">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-868">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-869">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-869">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-870">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-870">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-871">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-871">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-872">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-872">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-873">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-873">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-874">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-874">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-875">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-875">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-876">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-876">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-877">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-877">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-878">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-878">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-879">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-879">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-880">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-880">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-881">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-882">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-883">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-883">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-884">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-884">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-885">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-885">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-886">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-886">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="fbb75-887">\_<sup>PC</sup> DXGI_FORMAT_R32G32 type (15)</span><span class="sxs-lookup"><span data-stu-id="fbb75-887">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="fbb75-888">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-888">Target</span></span> | <span data-ttu-id="fbb75-889">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-889">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-890">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-891">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-891">64</span></span> |
| <span data-ttu-id="fbb75-892">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-892">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-893">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-893">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-894">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-894">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-895">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-895">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-896">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-896">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-897">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-897">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-898">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-898">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-899">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-899">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-900">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-901">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-901">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-902">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-902">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-903">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-904">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-905">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-905">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-906">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-907">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-907">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-908">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-908">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-909">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-910">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-910">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-911">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-912">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-913">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-914">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-915">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-915">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-916">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-917">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-918">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-919">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-920">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-921">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-922">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-923">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-924">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-924">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-925">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-925">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-926">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-926">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-927">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-927">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-928">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-928">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-929">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-929">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-930">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-930">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-931">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-931">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-932">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-933">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-934">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-935">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-935">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-936">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-936">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="fbb75-937">DXGI_FORMAT_R32G32 \_ float<sup>FNS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="fbb75-937">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="fbb75-938">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-938">Target</span></span> | <span data-ttu-id="fbb75-939">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-939">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-940">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-940">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-941">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-941">64</span></span> |
| <span data-ttu-id="fbb75-942">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-942">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-944">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-944">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-945">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-945">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-947">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-948">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-949">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-950">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-951">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-951">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-952">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-953">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-953">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-954">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-954">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-955">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-955">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-956">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-956">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-957">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-957">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-958">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-958">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-959">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-959">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-960">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-961">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-962">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-962">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-963">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-963">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-964">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-964">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-965">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-965">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-966">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-966">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-967">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-967">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-968">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-968">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-969">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-969">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-970">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-970">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-971">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-971">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-972">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-972">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-973">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-973">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-974">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-974">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-975">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-975">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-976">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-976">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-977">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-977">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-978">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-978">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-979">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-979">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-980">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-980">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-981">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-981">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-982">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-982">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-983">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-983">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-984">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-984">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-985">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-985">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-986">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-986">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-987">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-987">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-988">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-988">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="fbb75-989">DXGI_FORMAT_R32G32 \_ uint<sup>FNS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="fbb75-989">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="fbb75-990">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-990">Target</span></span> | <span data-ttu-id="fbb75-991">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-991">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-992">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-992">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-993">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-993">64</span></span> |
| <span data-ttu-id="fbb75-994">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-994">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-995">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-995">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-996">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-996">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-997">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-997">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-998">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-998">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-999">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-999">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1000">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1001">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1001">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1002">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1002">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1003">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1003">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1004">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1004">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1005">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1005">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1006">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1006">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1007">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1007">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1008">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1008">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1009">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1009">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1010">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1010">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1011">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1012">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1012">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1013">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1013">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1014">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1014">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1015">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1015">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1016">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1016">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1017">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1017">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1018">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1018">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1019">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1019">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1020">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1020">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1021">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1021">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1022">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1022">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1023">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1023">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1024">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1024">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1025">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1025">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1026">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1026">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1027">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1027">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1028">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1028">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1029">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1029">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1030">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1030">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1031">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1031">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1032">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1032">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1033">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1033">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1034">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1034">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1035">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1035">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1036">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1036">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1037">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1037">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1038">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1038">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="fbb75-1039">DXGI_FORMAT_R32G32 \_ Saint<sup>FNS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1039">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="fbb75-1040">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1040">Target</span></span> | <span data-ttu-id="fbb75-1041">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1041">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1042">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1042">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1043">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-1043">64</span></span> |
| <span data-ttu-id="fbb75-1044">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1044">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1045">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1045">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1046">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1046">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1047">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1047">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1048">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1048">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1049">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1049">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1050">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1050">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1051">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1051">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1052">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1053">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1053">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1054">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1054">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1055">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1055">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1056">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1056">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1057">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1057">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1058">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1058">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1059">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1059">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1060">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1060">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1061">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1061">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1062">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1062">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1063">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1063">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1064">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1064">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1065">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1065">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1066">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1066">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1067">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1067">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1068">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1068">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1069">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1069">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1070">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1070">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1071">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1071">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1072">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1072">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1073">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1073">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1074">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1074">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1075">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1075">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1076">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1076">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1077">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1078">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1079">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1080">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1081">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1081">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1082">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1083">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1084">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1084">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1085">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1085">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1086">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1086">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1087">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1087">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1088">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1088">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="fbb75-1089">\_<sup>PC</sup> DXGI_FORMAT_R32G8X24 type (19)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1089">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="fbb75-1090">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1090">Target</span></span> | <span data-ttu-id="fbb75-1091">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1091">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1092">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1093">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-1093">64</span></span> |
| <span data-ttu-id="fbb75-1094">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1094">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1095">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1095">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1096">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1096">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1097">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1097">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1098">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1098">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1099">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1099">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1100">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1100">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1101">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1101">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1102">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1102">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1103">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1103">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1104">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1105">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1106">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1107">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1107">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1108">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1109">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1109">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1110">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1110">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1111">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1112">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1113">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1114">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1115">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1116">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1117">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1117">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1118">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1119">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1120">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1121">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1122">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1123">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1124">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1124">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1125">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1125">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1126">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1126">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1127">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1127">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1128">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1128">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1129">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1129">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1130">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1130">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1131">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1131">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1132">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1132">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1133">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1133">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1134">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1134">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1135">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1135">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1136">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1136">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1137">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1137">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1138">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1138">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="fbb75-1139">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1139">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="fbb75-1140">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1140">Target</span></span> | <span data-ttu-id="fbb75-1141">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1141">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1142">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1142">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1143">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-1143">64</span></span> |
| <span data-ttu-id="fbb75-1144">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1144">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1145">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1145">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1146">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1146">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1147">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1147">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1148">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1148">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1149">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1149">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1150">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1151">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1151">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1152">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1152">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1153">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1153">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1154">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1154">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1155">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1155">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1156">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1156">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1157">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1157">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1158">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1158">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1159">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1159">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1160">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1160">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1161">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1161">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1162">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1163">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1164">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1165">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1166">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1167">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1167">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1168">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1168">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1169">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1169">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1170">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1170">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1171">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1171">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1172">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1172">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1173">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1173">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1174">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1174">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1175">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1175">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1176">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1176">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1177">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1178">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1179">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1180">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1181">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1181">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1182">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1183">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1184">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1184">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1185">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1185">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1186">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1186">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1187">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1187">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1188">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1188">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="fbb75-1189">DXGI_FORMAT_R32 \_ float \_ X8X24 \_ de type<sup>FNS</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1189">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="fbb75-1190">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1190">Target</span></span> | <span data-ttu-id="fbb75-1191">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1191">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1192">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1192">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1193">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-1193">64</span></span> |
| <span data-ttu-id="fbb75-1194">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1194">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1195">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1195">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1196">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1196">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1197">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1197">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1198">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1198">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1199">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1199">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1200">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1200">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1201">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1201">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1202">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1202">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1203">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1203">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1204">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1204">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1205">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1205">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1206">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1206">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1207">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1207">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1208">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1208">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1209">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1209">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1210">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1210">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1211">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1211">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1212">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1212">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1213">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1213">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1214">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1214">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1215">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1215">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1216">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1216">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1217">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1217">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1218">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1218">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1219">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1219">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1220">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1220">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1221">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1221">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1222">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1222">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1223">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1223">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1224">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1224">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1225">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1225">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1226">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1226">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1227">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1227">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1228">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1228">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1229">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1229">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1230">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1230">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1231">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1231">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1232">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1232">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1233">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1233">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1234">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1235">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1236">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1237">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1237">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1238">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1238">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="fbb75-1239">DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FNS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1239">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="fbb75-1240">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1240">Target</span></span> | <span data-ttu-id="fbb75-1241">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1241">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1242">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1242">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1243">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-1243">64</span></span> |
| <span data-ttu-id="fbb75-1244">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1244">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1245">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1245">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1246">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1246">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1247">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1247">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1248">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1248">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1249">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1249">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1250">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1250">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1251">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1252">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1253">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1253">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1254">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1254">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1255">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1256">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1257">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1257">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1258">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1259">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1259">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1260">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1260">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1261">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1261">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1262">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1262">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1263">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1263">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1264">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1264">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1265">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1265">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1266">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1266">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1267">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1267">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1268">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1268">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1269">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1269">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1270">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1270">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1271">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1271">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1272">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1272">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1273">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1273">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1274">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1274">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1275">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1275">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1276">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1276">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1277">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1277">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1278">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1278">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1279">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1279">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1280">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1280">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1281">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1281">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1282">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1283">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1283">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1284">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1284">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1285">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1285">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1286">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1286">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1287">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1287">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1288">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1288">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="fbb75-1289">\_<sup>PC</sup> DXGI_FORMAT_R10G10B10A2 type (23)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1289">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="fbb75-1290">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1290">Target</span></span> | <span data-ttu-id="fbb75-1291">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1291">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1292">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1292">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1293">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1293">32</span></span> |
| <span data-ttu-id="fbb75-1294">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1294">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1295">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1295">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1296">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1296">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1297">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1298">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1299">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1300">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1301">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1301">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1302">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1302">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1303">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1303">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1304">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1304">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1305">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1305">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1306">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1306">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1307">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1307">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1308">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1308">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1309">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1309">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1310">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1310">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1311">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1311">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1312">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1312">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1313">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1313">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1314">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1314">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1315">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1315">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1316">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1316">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1317">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1317">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1318">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1318">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1319">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1319">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1320">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1320">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1321">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1321">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1322">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1322">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1323">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1323">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1324">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1324">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1325">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1325">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1326">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1326">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1327">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1327">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1328">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1328">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1329">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1329">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1330">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1330">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1331">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1331">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1332">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1332">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1333">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1333">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1334">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1334">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1335">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1335">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1336">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1336">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1337">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1337">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1338">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1338">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="fbb75-1339">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1339">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="fbb75-1340">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1340">Target</span></span> | <span data-ttu-id="fbb75-1341">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1341">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1342">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1342">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1343">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1343">32</span></span> |
| <span data-ttu-id="fbb75-1344">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1344">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1345">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1345">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1346">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1346">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1347">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1348">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1349">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1350">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1350">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1351">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1351">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1352">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1352">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1353">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1353">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1354">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1354">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1355">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1355">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1356">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1356">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1357">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1357">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1358">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1358">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1359">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1359">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1360">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1360">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1361">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1361">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1362">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1362">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1363">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1363">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1364">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1364">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1365">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1365">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1366">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1366">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1367">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1367">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1368">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1368">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1369">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1369">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1370">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1370">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1371">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1371">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1372">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1372">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1373">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1373">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1374">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1374">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1375">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1375">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1376">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1376">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1377">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1377">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1378">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1378">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1379">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1379">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1380">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1380">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1381">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1381">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1382">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1382">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1383">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1383">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1384">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1385">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1386">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1387">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1387">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1389">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="fbb75-1390">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FNS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1390">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="fbb75-1391">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1391">Target</span></span> | <span data-ttu-id="fbb75-1392">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1392">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1393">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1394">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1394">32</span></span> |
| <span data-ttu-id="fbb75-1395">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1395">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1396">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1396">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1397">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1397">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1398">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1398">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1399">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1399">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1400">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1400">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1401">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1401">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1402">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1402">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1403">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1403">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1404">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1404">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1405">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1405">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1406">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1406">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1407">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1407">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1408">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1408">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1409">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1409">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1410">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1410">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1411">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1411">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1412">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1413">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1413">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1414">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1414">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1415">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1415">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1416">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1416">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1417">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1417">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1418">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1418">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1419">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1419">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1420">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1420">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1421">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1421">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1422">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1422">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1423">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1423">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1424">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1424">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1425">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1425">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1426">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1426">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1427">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1427">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1428">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1429">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1430">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1431">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1432">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1432">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1433">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1434">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1435">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1435">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1436">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1436">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1437">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1437">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1438">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1438">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1439">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1439">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="fbb75-1440">DXGI_FORMAT_R10G10B10 \_ XR \_ \_ de décalage a2 \_ UNORM<sup>FNS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1440">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="fbb75-1441">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1441">Target</span></span> | <span data-ttu-id="fbb75-1442">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1442">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1443">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1443">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1444">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1444">32</span></span> |
| <span data-ttu-id="fbb75-1445">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1445">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1446">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1446">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1447">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1447">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1448">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1448">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1449">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1449">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1450">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1450">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1451">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1451">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1453">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1454">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1454">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1455">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1456">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1457">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1458">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1459">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1460">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1460">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1461">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1461">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1462">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1462">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1463">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1463">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1464">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1465">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1466">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1467">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1468">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1468">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1469">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1470">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1471">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1472">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1474">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1475">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1476">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1477">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1477">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1478">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1478">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1479">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1479">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1480">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1481">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1482">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1482">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1483">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1484">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1485">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1486">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1487">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1488">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1488">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1489">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="fbb75-1490">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1490">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="fbb75-1491">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1491">Target</span></span> | <span data-ttu-id="fbb75-1492">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1492">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1493">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1494">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1494">32</span></span> |
| <span data-ttu-id="fbb75-1495">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1495">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1496">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1496">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1497">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1498">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1499">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1500">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1501">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1502">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1503">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1504">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1505">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1506">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1507">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1508">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1508">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1509">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1510">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1510">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1511">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1512">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1513">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1514">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1515">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1516">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1517">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1518">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1518">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1519">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1520">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1521">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1522">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1524">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1525">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1526">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1527">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1528">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1528">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1529">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1529">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1530">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1530">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1531">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1531">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1532">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1532">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1533">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1533">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1534">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1534">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1535">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1535">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1536">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1536">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1537">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1537">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1538">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1538">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1539">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1539">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="fbb75-1540">\_<sup>PC</sup> DXGI_FORMAT_R8G8B8A8 type (27)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1540">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="fbb75-1541">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1541">Target</span></span> | <span data-ttu-id="fbb75-1542">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1542">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1543">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1543">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1544">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1544">32</span></span> |
| <span data-ttu-id="fbb75-1545">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1545">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1546">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1546">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1547">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1548">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1549">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1550">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1551">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1552">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1552">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1553">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1553">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1554">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1554">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1555">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1555">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1556">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1556">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1557">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1557">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1558">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1558">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1559">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1559">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1560">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1560">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1561">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1561">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1562">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1562">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1563">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1563">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1564">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1565">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1566">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1567">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1568">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1568">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1569">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1570">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1571">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1572">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1573">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1574">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1575">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1576">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1577">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1577">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1578">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1578">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1579">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1579">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1580">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1580">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1581">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1581">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1582">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1582">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1583">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1583">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1584">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1584">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1585">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1585">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1586">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1586">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1587">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1587">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1588">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1588">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1589">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="fbb75-1590">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1590">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="fbb75-1591">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1591">Target</span></span> | <span data-ttu-id="fbb75-1592">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1592">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1593">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1594">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1594">32</span></span> |
| <span data-ttu-id="fbb75-1595">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1595">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1597">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1597">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1598">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1598">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1600">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1601">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1603">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1605">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1605">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1607">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1609">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1609">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1611">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1611">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1613">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1614">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1615">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1615">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1616">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1617">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1617">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1619">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1619">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1621">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1621">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1623">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1623">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1625">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1625">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1626">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1626">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1627">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1627">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1628">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1628">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1629">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1629">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1630">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1630">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1631">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1631">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1632">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1632">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1633">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1633">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1634">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1634">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1635">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1635">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1636">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1636">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1637">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1637">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1638">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1638">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1640">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1640">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-1642">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1642">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-1644">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1644">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-1646">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1646">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1648">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1648">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1649">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1649">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1651">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1651">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1652">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1652">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1653">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1653">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-1655">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1655">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1657">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1657">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1659">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1659">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="fbb75-1660">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRVB<sup>FNS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1660">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="fbb75-1661">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1661">Target</span></span> | <span data-ttu-id="fbb75-1662">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1662">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1663">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1663">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1664">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1664">32</span></span> |
| <span data-ttu-id="fbb75-1665">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1665">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1667">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1667">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1668">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1668">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1669">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1669">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1670">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1670">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1671">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1671">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1672">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1672">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1674">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1674">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1676">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1676">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1678">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1678">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1680">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1680">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1682">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1682">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1683">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1683">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1684">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1684">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1685">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1685">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1686">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1686">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1688">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1688">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1690">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1690">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1692">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1692">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1694">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1694">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1695">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1695">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1696">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1696">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1697">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1697">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1698">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1698">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1699">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1699">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1700">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1700">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1701">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1701">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1702">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1702">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1703">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1703">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1704">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1704">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1705">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1705">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1706">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1706">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1707">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1707">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1709">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1709">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-1711">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1711">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-1713">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1713">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-1715">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1715">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1717">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1717">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1718">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1718">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1720">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1720">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1721">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1721">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1722">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1722">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-1724">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1724">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1726">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1726">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1728">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1728">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="fbb75-1729">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1729">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="fbb75-1730">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1730">Target</span></span> | <span data-ttu-id="fbb75-1731">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1731">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1732">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1732">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1733">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1733">32</span></span> |
| <span data-ttu-id="fbb75-1734">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1734">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1736">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1736">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1737">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1737">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1739">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1739">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1740">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1740">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1741">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1741">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1742">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1742">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1743">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1743">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1744">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1744">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1745">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1745">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1746">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1746">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1747">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1748">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1749">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1749">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1750">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1750">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1751">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1751">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1752">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1752">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1753">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1753">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1754">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1754">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1755">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1755">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1756">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1756">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1757">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1757">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1758">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1758">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1759">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1759">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1760">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1760">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1761">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1761">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1762">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1762">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1763">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1763">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1764">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1764">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1765">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1765">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1766">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1766">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1767">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1767">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1768">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1768">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1769">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1770">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1771">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1772">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1773">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1773">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1774">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1775">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1775">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1776">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1777">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1778">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1779">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1779">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1780">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="fbb75-1781">DXGI_FORMAT_R8G8B8A8 \_ ronfler<sup>FNS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1781">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="fbb75-1782">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1782">Target</span></span> | <span data-ttu-id="fbb75-1783">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1784">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1785">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1785">32</span></span> |
| <span data-ttu-id="fbb75-1786">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1786">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1788">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1789">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1789">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1790">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1790">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1791">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1791">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1792">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1792">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1793">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1793">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1796">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1798">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1798">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1800">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1800">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1802">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1803">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1804">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1804">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1805">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1806">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1806">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1808">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1809">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1810">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1811">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1812">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1813">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1814">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1815">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1815">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1816">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1816">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1817">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1817">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1818">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1818">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1819">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1819">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1820">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1820">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1821">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1821">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1822">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1822">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1823">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1823">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1824">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1824">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-1826">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1826">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1827">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1827">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1828">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1828">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1829">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1829">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1830">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1830">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1831">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1831">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1832">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1832">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1833">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1833">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1834">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1834">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1835">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1835">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1836">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1836">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1837">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="fbb75-1838">DXGI_FORMAT_R8G8B8A8 \_ Saint<sup>FNS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1838">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="fbb75-1839">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1839">Target</span></span> | <span data-ttu-id="fbb75-1840">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1840">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1841">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1842">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1842">32</span></span> |
| <span data-ttu-id="fbb75-1843">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1843">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1844">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1844">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1845">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1845">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1846">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1846">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1847">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1847">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1848">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1848">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1849">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1849">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1850">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1850">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1851">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1851">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1852">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1852">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1853">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1853">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1854">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1855">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1856">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1857">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1858">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1858">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1859">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1859">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1860">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1860">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1861">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1861">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1862">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1862">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1863">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1863">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1864">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1864">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1865">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1865">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1866">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1866">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1867">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1867">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1868">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1868">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1869">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1869">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1870">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1870">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1871">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1871">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1872">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1872">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1873">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1873">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1874">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1874">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1875">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1875">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1876">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1876">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1877">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1877">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1878">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1878">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1879">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1879">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1880">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1880">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1881">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1881">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1882">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1882">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1883">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1883">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1884">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1884">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1885">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1885">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1886">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1886">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1887">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1887">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="fbb75-1888">\_<sup>PC</sup> DXGI_FORMAT_R16G16 type (33)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1888">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="fbb75-1889">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1889">Target</span></span> | <span data-ttu-id="fbb75-1890">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1890">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1891">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1891">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1892">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1892">32</span></span> |
| <span data-ttu-id="fbb75-1893">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1893">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1894">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1894">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1895">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1896">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1897">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1898">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1899">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1899">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1900">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1900">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1901">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1901">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1902">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1902">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1903">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1903">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1904">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1904">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1905">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1905">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1906">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1906">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1907">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1907">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1908">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1908">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1909">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1909">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1910">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1910">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1911">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1911">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1912">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1912">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1913">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1913">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1914">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1914">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1915">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1915">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1916">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1916">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1917">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1917">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1918">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1918">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1919">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1919">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1920">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1920">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1921">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1921">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1922">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1922">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1923">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1923">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1924">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1924">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1925">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1925">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1926">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1926">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1927">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1927">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1928">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1928">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1929">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1929">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1930">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1930">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1931">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1931">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1932">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1932">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1933">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1933">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1934">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1934">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1935">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1935">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1936">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1936">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1937">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="fbb75-1938">DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1938">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="fbb75-1939">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1939">Target</span></span> | <span data-ttu-id="fbb75-1940">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1940">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1941">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1942">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1942">32</span></span> |
| <span data-ttu-id="fbb75-1943">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1943">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1944">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1944">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1945">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1945">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1946">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1946">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1947">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1947">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1948">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1948">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1949">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1949">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-1950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1950">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-1951">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-1951">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-1952">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1952">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-1953">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1954">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1955">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-1956">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-1956">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-1957">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-1957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-1958">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-1958">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-1959">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-1959">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-1960">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1960">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1961">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1961">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1962">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-1962">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-1963">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-1963">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-1964">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-1964">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1965">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-1965">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-1966">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-1966">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-1967">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1967">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-1968">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1968">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-1969">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-1969">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-1970">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1970">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-1971">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-1971">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-1972">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1972">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-1973">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-1973">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1974">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-1974">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-1975">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-1975">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-1976">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-1976">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1977">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-1977">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-1978">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-1978">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-1979">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-1979">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-1980">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-1980">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-1981">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-1981">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-1982">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-1982">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-1983">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1983">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-1984">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1984">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-1985">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-1985">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-1986">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1986">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-1987">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-1987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="fbb75-1988">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1988">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="fbb75-1989">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-1989">Target</span></span> | <span data-ttu-id="fbb75-1990">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-1990">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-1991">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-1991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-1992">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-1992">32</span></span> |
| <span data-ttu-id="fbb75-1993">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-1993">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-1994">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-1994">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1995">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1995">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1996">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-1996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1997">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-1997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-1998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1998">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-1999">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-1999">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2000">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2000">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2001">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2001">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2002">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2002">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2003">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2003">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2004">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2004">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2005">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2005">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2006">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2006">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2007">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2007">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2008">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2008">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2009">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2009">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2010">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2010">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2011">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2011">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2012">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2013">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2014">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2015">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2016">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2016">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2017">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2018">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2019">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2020">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2021">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2022">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2023">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2023">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2024">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2024">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2025">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2025">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2026">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2026">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2027">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2027">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2028">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2028">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2029">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2029">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2030">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2030">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2031">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2031">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2032">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2032">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2033">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2033">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2034">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2034">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2035">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2035">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2036">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2036">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2037">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2037">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="fbb75-2038">DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2038">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="fbb75-2039">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2039">Target</span></span> | <span data-ttu-id="fbb75-2040">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2040">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2041">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2041">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2042">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2042">32</span></span> |
| <span data-ttu-id="fbb75-2043">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2043">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2044">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2044">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2045">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2045">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2046">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2046">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2047">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2047">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2048">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2048">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2049">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2049">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2050">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2051">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2052">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2053">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2054">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2055">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2056">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2056">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2057">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2058">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2058">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2059">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2060">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2061">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2062">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2063">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2064">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2065">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2066">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2066">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2067">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2068">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2069">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2070">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2072">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2073">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2074">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2075">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2075">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2076">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2076">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2077">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2077">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2078">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2078">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2079">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2079">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2080">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2080">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2081">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2081">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2082">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2082">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2083">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2083">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2084">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2084">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2085">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2085">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2086">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2086">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2087">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2087">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="fbb75-2088">DXGI_FORMAT_R16G16 \_ ronfler<sup>FNS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2088">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="fbb75-2089">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2089">Target</span></span> | <span data-ttu-id="fbb75-2090">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2090">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2091">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2091">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2092">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2092">32</span></span> |
| <span data-ttu-id="fbb75-2093">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2093">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2095">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2095">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2096">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2096">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2098">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2098">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2099">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2099">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2100">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2100">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2101">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2101">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2103">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2104">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2105">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2105">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2107">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2107">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2108">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2108">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2109">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2109">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2110">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2110">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2111">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2111">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2112">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2112">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2114">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2114">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2115">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2115">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2116">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2116">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2117">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2117">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2118">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2118">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2119">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2119">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2120">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2120">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2121">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2121">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2122">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2122">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2123">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2123">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2124">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2124">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2125">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2125">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2126">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2126">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2127">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2127">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2128">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2128">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2129">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2129">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2130">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2130">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2132">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2132">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2133">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2133">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2134">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2134">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2135">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2135">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2136">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2136">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2137">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2137">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2138">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2138">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2139">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2139">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2140">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2140">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2141">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2141">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2142">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2142">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2143">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2143">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="fbb75-2144">DXGI_FORMAT_R16G16 \_ Saint<sup>FNS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2144">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="fbb75-2145">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2145">Target</span></span> | <span data-ttu-id="fbb75-2146">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2146">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2147">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2148">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2148">32</span></span> |
| <span data-ttu-id="fbb75-2149">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2149">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2151">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2151">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2152">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2152">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2154">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2154">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2155">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2155">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2156">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2156">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2157">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2157">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2158">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2158">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2159">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2159">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2160">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2160">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2161">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2162">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2163">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2164">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2164">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2165">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2166">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2166">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2167">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2167">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2168">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2168">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2169">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2169">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2170">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2170">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2171">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2171">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2172">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2172">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2173">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2173">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2174">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2174">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2175">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2175">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2176">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2176">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2177">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2177">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2178">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2178">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2179">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2179">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2180">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2180">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2181">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2181">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2182">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2182">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2183">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2183">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2184">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2185">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2186">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2187">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2188">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2188">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2189">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2190">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2191">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2191">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2192">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2192">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2193">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2193">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2194">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2194">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2195">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="fbb75-2196">\_<sup>PC</sup> DXGI_FORMAT_R32 type (39)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2196">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="fbb75-2197">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2197">Target</span></span> | <span data-ttu-id="fbb75-2198">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2198">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2199">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2200">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2200">32</span></span> |
| <span data-ttu-id="fbb75-2201">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2201">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2202">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2202">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2203">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2204">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2205">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2206">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2207">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2208">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2209">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2209">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2210">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2210">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2211">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2211">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2212">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2212">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2213">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2213">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2214">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2214">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2215">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2215">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2216">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2216">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2217">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2217">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2218">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2218">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2219">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2219">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2220">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2220">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2221">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2221">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2222">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2222">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2223">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2223">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2224">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2224">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2225">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2225">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2226">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2226">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2227">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2227">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2228">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2228">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2229">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2229">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2230">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2230">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2231">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2231">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2232">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2232">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2233">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2233">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2234">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2234">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2235">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2235">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2236">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2236">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2237">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2237">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2238">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2238">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2239">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2239">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2240">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2240">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2241">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2241">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2242">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2242">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2243">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2243">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2244">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2244">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2245">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2245">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="fbb75-2246">DXGI_FORMAT_D32 \_ float<sup>FNS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2246">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="fbb75-2247">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2247">Target</span></span> | <span data-ttu-id="fbb75-2248">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2248">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2249">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2249">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2250">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2250">32</span></span> |
| <span data-ttu-id="fbb75-2251">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2251">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2252">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2252">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2253">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2253">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2254">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2254">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2255">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2255">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2256">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2256">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2257">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2258">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2258">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2259">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2259">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2260">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2260">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2261">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2261">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2262">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2262">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2263">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2263">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2264">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2264">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2265">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2265">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2266">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2266">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2267">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2267">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2268">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2268">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2269">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2269">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2270">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2270">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2271">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2271">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2272">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2272">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2273">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2273">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2274">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2274">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2275">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2275">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2276">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2276">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2277">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2277">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2278">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2278">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2279">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2279">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2280">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2280">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2281">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2281">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2282">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2282">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2283">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2283">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2284">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2284">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2285">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2285">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2286">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2286">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2287">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2287">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2288">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2288">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2289">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2289">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2290">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2290">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2291">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2291">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2292">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2292">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2293">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2293">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2294">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2294">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2295">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2295">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="fbb75-2296">DXGI_FORMAT_R32 \_ float<sup>FNS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2296">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="fbb75-2297">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2297">Target</span></span> | <span data-ttu-id="fbb75-2298">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2298">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2299">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2299">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2300">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2300">32</span></span> |
| <span data-ttu-id="fbb75-2301">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2301">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2303">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2303">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2304">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2304">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2306">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2306">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2307">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2307">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2308">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2308">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2309">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2309">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2310">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2310">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2311">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2311">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2312">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2312">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2313">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2313">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2314">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2314">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2315">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2315">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2316">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2316">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2317">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2317">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2318">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2318">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2319">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2320">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2321">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2322">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2323">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2324">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2325">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2326">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2326">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2327">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2328">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2329">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2330">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2332">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2333">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2334">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2335">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2335">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2336">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2336">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2337">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2337">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2338">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2338">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2339">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2339">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2340">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2340">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2341">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2341">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2342">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2342">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2343">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2343">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2344">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2344">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2345">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2345">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2346">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2346">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2347">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2347">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="fbb75-2348">DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2348">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="fbb75-2349">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2349">Target</span></span> | <span data-ttu-id="fbb75-2350">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2350">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2351">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2351">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2352">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2352">32</span></span> |
| <span data-ttu-id="fbb75-2353">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2353">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2354">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2354">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2355">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2355">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2356">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2356">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2357">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2357">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2358">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2358">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2359">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2359">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2360">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2361">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2362">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2362">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2363">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2363">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2364">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2364">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2365">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2365">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2366">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2366">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2367">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2367">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2368">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2368">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2369">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2369">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2370">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2371">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2371">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2372">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2372">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2373">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2373">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2374">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2374">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2375">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2375">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2376">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2376">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2377">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2377">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2378">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2378">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2379">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2379">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2380">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2380">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2381">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2381">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2382">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2382">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2383">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2383">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2384">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2384">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2385">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2385">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2386">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2386">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2387">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2387">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2388">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2388">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2389">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2389">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2390">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2390">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2391">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2391">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2392">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2392">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2393">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2393">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2394">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2394">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2395">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2395">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2396">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2396">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2397">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2397">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="fbb75-2398">DXGI_FORMAT_R32 \_ Saint<sup>FNS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2398">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="fbb75-2399">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2399">Target</span></span> | <span data-ttu-id="fbb75-2400">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2400">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2401">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2401">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2402">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2402">32</span></span> |
| <span data-ttu-id="fbb75-2403">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2403">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2404">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2404">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2405">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2405">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2406">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2406">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2407">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2407">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2408">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2408">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2409">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2409">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2410">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2410">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2411">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2411">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2412">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2412">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2413">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2414">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2415">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2416">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2416">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2417">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2418">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2418">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2419">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2419">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2420">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2420">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2421">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2421">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2422">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2422">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2423">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2423">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2424">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2424">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2425">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2425">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2426">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2426">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2427">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2427">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2428">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2428">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2429">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2429">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2430">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2430">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2431">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2431">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2432">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2432">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2433">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2433">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2434">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2434">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2435">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2435">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2436">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2437">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2438">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2439">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2440">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2440">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2441">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2442">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2442">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2443">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2443">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2444">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2444">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2445">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2445">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2446">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2446">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2447">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2447">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="fbb75-2448">\_<sup>PC</sup> DXGI_FORMAT_R24G8 type (44)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2448">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="fbb75-2449">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2449">Target</span></span> | <span data-ttu-id="fbb75-2450">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2450">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2451">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2451">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2452">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2452">32</span></span> |
| <span data-ttu-id="fbb75-2453">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2453">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2454">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2454">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2455">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2455">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2456">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2456">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2457">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2457">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2458">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2458">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2459">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2459">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2460">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2460">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2461">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2461">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2462">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2462">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2463">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2463">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2464">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2464">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2465">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2465">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2466">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2466">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2467">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2467">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2468">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2468">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2469">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2470">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2471">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2472">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2473">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2474">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2475">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2476">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2476">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2477">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2478">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2479">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2480">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2481">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2482">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2483">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2484">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2485">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2485">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2486">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2486">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2487">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2487">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2488">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2488">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2489">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2489">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2490">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2490">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2491">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2491">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2492">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2492">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2493">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2494">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2495">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2496">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2496">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2497">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="fbb75-2498">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2498">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="fbb75-2499">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2499">Target</span></span> | <span data-ttu-id="fbb75-2500">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2500">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2501">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2502">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2502">32</span></span> |
| <span data-ttu-id="fbb75-2503">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2503">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2505">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2505">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2506">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2507">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2508">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2509">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2510">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2512">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2513">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2514">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2515">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2516">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2517">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2518">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2518">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2519">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2520">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2520">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2521">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2522">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2523">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2524">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2525">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2525">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2527">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2527">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2528">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2528">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2529">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2529">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2530">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2530">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2531">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2531">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2532">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2532">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2533">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2533">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2534">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2534">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2535">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2535">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2536">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2536">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2537">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2537">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2538">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2538">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2539">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2539">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-2541">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2541">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-2543">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2543">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-2545">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2545">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2546">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2546">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2547">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2547">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2548">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2548">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2549">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2549">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2550">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2550">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2551">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2551">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2552">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2552">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2553">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2553">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="fbb75-2554">DXGI_FORMAT_R24 \_ UNORM \_ x8 \_ de type<sup>FNS</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2554">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="fbb75-2555">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2555">Target</span></span> | <span data-ttu-id="fbb75-2556">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2556">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2557">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2557">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2558">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2558">32</span></span> |
| <span data-ttu-id="fbb75-2559">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2559">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2560">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2560">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2561">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2561">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2562">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2563">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2564">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2565">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2565">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2566">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2567">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2567">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2568">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2568">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2569">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2569">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2570">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2570">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2571">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2571">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2572">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2572">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2573">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2573">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2574">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2574">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2575">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2575">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2576">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2576">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2577">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2577">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2578">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2578">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2579">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2579">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2580">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2580">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2581">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2581">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2582">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2582">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2583">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2583">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2584">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2584">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2585">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2585">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2586">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2586">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2587">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2587">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2588">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2588">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2589">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2589">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2590">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2590">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2591">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2591">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2592">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2592">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2593">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2593">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2594">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2594">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2595">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2595">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2596">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2596">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2597">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2597">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2598">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2598">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2599">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2600">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2601">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2602">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2602">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2603">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="fbb75-2604">DXGI_FORMAT_X24 \_ \_ G8 \_ UINT<sup>FNS</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2604">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="fbb75-2605">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2605">Target</span></span> | <span data-ttu-id="fbb75-2606">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2606">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2607">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2608">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-2608">32</span></span> |
| <span data-ttu-id="fbb75-2609">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2609">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2610">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2610">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2611">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2611">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2612">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2612">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2613">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2613">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2614">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2614">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2615">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2616">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2616">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2617">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2617">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2618">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2618">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2619">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2620">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2620">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2621">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2621">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2622">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2622">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2623">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2623">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2624">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2624">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2625">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2625">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2626">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2626">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2627">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2627">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2628">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2628">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2629">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2629">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2630">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2630">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2631">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2631">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2632">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2632">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2633">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2633">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2634">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2634">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2635">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2635">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2636">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2636">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2637">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2637">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2638">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2638">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2639">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2639">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2640">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2640">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2641">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2641">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2642">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2642">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2643">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2643">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2644">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2644">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2645">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2645">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2646">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2646">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2647">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2647">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2648">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2648">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2649">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2649">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2650">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2650">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2651">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2651">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2652">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2652">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2653">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2653">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="fbb75-2654">\_<sup>PC</sup> DXGI_FORMAT_R8G8 type (48)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2654">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="fbb75-2655">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2655">Target</span></span> | <span data-ttu-id="fbb75-2656">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2656">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2657">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2657">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2658">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-2658">16</span></span> |
| <span data-ttu-id="fbb75-2659">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2659">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2660">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2660">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2661">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2661">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2662">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2662">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2663">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2663">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2664">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2664">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2665">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2666">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2666">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2667">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2667">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2668">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2668">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2669">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2669">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2670">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2670">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2671">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2671">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2672">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2672">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2673">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2673">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2674">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2674">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2675">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2675">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2676">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2676">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2677">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2677">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2678">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2678">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2679">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2679">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2680">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2680">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2681">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2681">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2682">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2682">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2683">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2683">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2684">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2684">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2685">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2685">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2686">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2686">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2687">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2687">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2688">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2688">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2689">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2689">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2690">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2690">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2691">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2691">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2692">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2693">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2694">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2695">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2696">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2696">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2697">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2698">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2699">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2700">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2700">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2701">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2701">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2702">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2702">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2703">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2703">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="fbb75-2704">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2704">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="fbb75-2705">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2705">Target</span></span> | <span data-ttu-id="fbb75-2706">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2706">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2707">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2707">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2708">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-2708">16</span></span> |
| <span data-ttu-id="fbb75-2709">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2709">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2711">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2711">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2712">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2712">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2713">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2713">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2714">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2714">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2715">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2715">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2716">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2718">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2719">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2719">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2720">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2720">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2722">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2722">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2724">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2724">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2725">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2725">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2726">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2726">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2727">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2727">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2728">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2728">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2729">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2729">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2730">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2730">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2732">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2732">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2734">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2734">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2735">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2735">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2736">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2736">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2737">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2737">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2738">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2738">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2739">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2739">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2740">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2740">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2741">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2741">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2742">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2742">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2743">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2743">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2744">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2744">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2745">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2745">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2746">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2746">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2747">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2747">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2749">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2749">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2750">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2750">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2751">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2751">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2752">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2752">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2753">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2753">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2754">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2754">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2755">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2755">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2756">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2756">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2757">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2757">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2758">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2758">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2759">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2759">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2761">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2761">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="fbb75-2762">DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2762">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="fbb75-2763">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2763">Target</span></span> | <span data-ttu-id="fbb75-2764">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2764">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2765">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2765">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2766">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-2766">16</span></span> |
| <span data-ttu-id="fbb75-2767">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2767">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2768">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2768">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2769">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2769">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2770">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2771">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2772">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2773">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2773">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2774">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2775">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2775">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2776">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2776">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2777">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2777">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2778">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2778">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2779">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2779">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2780">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2780">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2781">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2781">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2782">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2782">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2783">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2783">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2784">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2784">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2785">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2786">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2787">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2788">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2789">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2790">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2790">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2791">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2792">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2793">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2794">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2795">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2796">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2797">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2798">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2799">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2799">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2800">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2801">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2802">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2803">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2804">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2804">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2805">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2806">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2807">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2808">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2808">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2809">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2810">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2810">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2811">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="fbb75-2812">DXGI_FORMAT_R8G8 \_ ronfler<sup>FNS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2812">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="fbb75-2813">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2813">Target</span></span> | <span data-ttu-id="fbb75-2814">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2815">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2816">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-2816">16</span></span> |
| <span data-ttu-id="fbb75-2817">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2817">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2819">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2820">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2821">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2822">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2823">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2824">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2826">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2827">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2828">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2828">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2830">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2830">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2832">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2833">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2834">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2835">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2836">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2836">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2838">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2840">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2841">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2842">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2843">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2844">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2845">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2845">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2846">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2847">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2848">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2849">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2850">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2851">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2852">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2852">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2853">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2853">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2854">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2854">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-2856">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2857">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2858">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2859">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2860">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2860">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2861">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2862">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2862">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2863">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2864">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2864">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2865">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2865">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2866">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2866">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2867">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2867">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="fbb75-2868">DXGI_FORMAT_R8G8 \_ Saint<sup>FNS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2868">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="fbb75-2869">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2869">Target</span></span> | <span data-ttu-id="fbb75-2870">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2870">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2871">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2871">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2872">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-2872">16</span></span> |
| <span data-ttu-id="fbb75-2873">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2873">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2874">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2874">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2875">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2876">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2877">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2878">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2879">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2880">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2881">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2882">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2883">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2884">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2885">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2886">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2886">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2887">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2888">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2888">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2889">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2890">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2891">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2892">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2893">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2894">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2895">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2896">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2896">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2897">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2898">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2899">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2900">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2902">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2903">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2904">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2905">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2905">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2906">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2906">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2907">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2907">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2908">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2908">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2909">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2909">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2910">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2910">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2911">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2911">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2912">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2912">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2913">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2914">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2915">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2916">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2917">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2917">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="fbb75-2918">\_<sup>PC</sup> DXGI_FORMAT_R16 type (53)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2918">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="fbb75-2919">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2919">Target</span></span> | <span data-ttu-id="fbb75-2920">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2920">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2921">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2921">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2922">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-2922">16</span></span> |
| <span data-ttu-id="fbb75-2923">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2923">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2924">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2924">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2925">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2925">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2926">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2926">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2927">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2927">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2928">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2928">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2929">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2929">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2930">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2930">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2931">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2931">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2932">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2932">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2933">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2934">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2935">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2936">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2936">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2937">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2938">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2938">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2939">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2939">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2940">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2940">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2941">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2941">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2942">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2942">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2943">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2943">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2944">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2944">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2945">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2945">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2946">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2946">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2947">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2947">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2948">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2948">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2949">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2949">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-2950">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2950">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-2951">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-2951">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-2952">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2952">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-2953">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2953">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2954">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-2954">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-2955">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2955">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-2956">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-2956">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2957">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2957">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2958">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-2958">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-2959">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-2959">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-2960">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-2960">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-2961">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-2961">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-2962">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-2962">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-2963">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-2964">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2964">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-2965">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-2965">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-2966">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2966">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-2967">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-2967">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="fbb75-2968">DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2968">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="fbb75-2969">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-2969">Target</span></span> | <span data-ttu-id="fbb75-2970">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-2970">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-2971">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2971">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-2972">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-2972">16</span></span> |
| <span data-ttu-id="fbb75-2973">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-2973">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-2974">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-2974">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2975">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2975">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2976">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-2976">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2977">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-2977">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-2978">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2978">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-2979">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2979">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-2980">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-2980">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-2981">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-2981">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-2982">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2982">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-2983">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2983">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2984">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2984">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2985">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-2985">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-2986">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-2986">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-2987">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-2987">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-2988">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-2988">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-2989">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-2989">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-2990">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-2990">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2991">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-2991">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-2992">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-2992">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-2993">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-2993">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-2994">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-2994">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2995">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-2995">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-2996">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-2996">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-2997">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2997">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-2998">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-2998">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-2999">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-2999">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3000">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3000">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3001">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3001">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3002">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3002">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3003">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3003">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3004">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3004">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3005">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3005">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3006">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3007">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3008">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3009">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3010">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3010">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3011">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3012">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3013">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3014">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3015">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3016">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3016">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3017">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="fbb75-3018">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3018">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="fbb75-3019">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3019">Target</span></span> | <span data-ttu-id="fbb75-3020">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3020">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3021">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3022">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-3022">16</span></span> |
| <span data-ttu-id="fbb75-3023">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3023">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3025">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3025">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3026">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3026">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3027">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3027">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3028">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3028">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3029">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3029">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3030">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3030">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3032">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3032">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3033">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3033">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3034">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3034">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3035">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3035">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3036">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3036">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3037">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3037">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3038">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3038">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3039">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3039">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3040">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3040">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3041">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3041">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3042">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3043">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3043">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3044">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3044">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3045">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3045">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3047">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3047">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3048">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3048">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3049">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3049">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3050">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3050">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3051">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3051">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3052">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3052">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3053">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3053">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3054">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3054">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3055">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3055">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3056">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3056">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3057">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3057">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3058">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3058">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3059">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3059">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-3061">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3061">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-3063">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3063">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-3065">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3066">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3066">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3067">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3068">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3069">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3070">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3071">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3072">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3072">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3073">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3073">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="fbb75-3074">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3074">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="fbb75-3075">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3075">Target</span></span> | <span data-ttu-id="fbb75-3076">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3076">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3077">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3077">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3078">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-3078">16</span></span> |
| <span data-ttu-id="fbb75-3079">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3079">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3080">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3080">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3081">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3081">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3082">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3082">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3083">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3083">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3084">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3084">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3085">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3086">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3086">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3087">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3087">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3088">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3088">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3089">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3089">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3090">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3090">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3091">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3091">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3092">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3092">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3093">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3093">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3094">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3094">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3095">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3096">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3097">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3098">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3099">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3100">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3101">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3102">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3102">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3103">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3104">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3105">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3106">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3108">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3109">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3110">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3111">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3111">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3112">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3112">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3113">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3113">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3114">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3114">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3115">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3115">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3116">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3116">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3117">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3117">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3118">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3118">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3119">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3120">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3121">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3122">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3122">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3123">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3123">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="fbb75-3124">DXGI_FORMAT_R16 \_ uint<sup>FNS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3124">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="fbb75-3125">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3125">Target</span></span> | <span data-ttu-id="fbb75-3126">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3126">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3127">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3127">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3128">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-3128">16</span></span> |
| <span data-ttu-id="fbb75-3129">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3129">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3131">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3131">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3132">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3132">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3133">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3133">Input Assembler Index Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3135">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3135">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3136">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3136">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3137">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3137">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3138">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3138">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3139">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3140">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3140">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3141">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3141">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3142">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3142">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3143">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3143">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3144">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3144">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3145">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3145">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3146">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3146">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3147">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3147">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3148">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3148">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3149">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3149">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3150">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3150">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3151">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3151">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3152">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3152">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3153">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3153">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3154">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3154">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3155">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3155">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3156">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3156">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3157">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3157">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3158">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3158">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3159">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3159">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3160">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3160">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3161">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3161">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3162">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3162">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3163">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3163">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3164">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3164">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3165">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3165">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3166">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3166">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3167">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3167">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3168">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3168">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3169">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3169">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3170">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3170">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3171">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3171">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3172">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3172">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3173">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3173">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3174">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3174">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3175">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="fbb75-3176">DXGI_FORMAT_R16 \_ ronfler<sup>FNS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3176">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="fbb75-3177">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3177">Target</span></span> | <span data-ttu-id="fbb75-3178">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3178">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3179">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3180">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-3180">16</span></span> |
| <span data-ttu-id="fbb75-3181">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3181">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3182">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3182">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3183">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3183">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3184">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3185">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3185">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3186">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3186">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3187">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3188">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3188">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3189">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3190">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3190">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3191">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3191">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3192">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3192">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3193">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3193">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3194">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3194">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3195">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3195">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3196">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3196">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3197">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3198">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3199">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3200">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3201">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3202">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3203">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3204">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3204">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3205">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3206">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3207">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3208">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3210">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3211">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3212">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3213">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3213">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3214">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3214">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3215">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3215">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3216">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3216">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3217">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3217">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3218">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3218">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3219">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3219">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3220">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3220">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3221">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3221">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3222">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3222">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3223">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3223">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3224">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3224">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3225">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3225">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="fbb75-3226">DXGI_FORMAT_R16 \_ Saint<sup>FNS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3226">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="fbb75-3227">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3227">Target</span></span> | <span data-ttu-id="fbb75-3228">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3228">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3229">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3229">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3230">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-3230">16</span></span> |
| <span data-ttu-id="fbb75-3231">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3231">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3232">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3232">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3233">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3233">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3234">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3234">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3235">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3235">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3236">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3236">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3237">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3237">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3238">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3238">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3239">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3240">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3240">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3241">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3241">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3242">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3242">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3243">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3243">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3244">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3244">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3245">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3245">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3246">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3246">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3247">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3247">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3248">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3248">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3249">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3249">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3250">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3250">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3251">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3251">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3252">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3252">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3253">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3253">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3254">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3254">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3255">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3255">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3256">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3256">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3257">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3257">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3258">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3258">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3259">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3259">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3260">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3260">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3261">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3261">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3262">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3262">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3263">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3263">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3264">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3264">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3265">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3265">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3266">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3266">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3267">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3267">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3268">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3268">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3269">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3269">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3270">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3270">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3271">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3271">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3272">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3272">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3273">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3273">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3274">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3274">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3275">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3275">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="fbb75-3276">\_<sup>PC</sup> DXGI_FORMAT_R8 type (60)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3276">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="fbb75-3277">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3277">Target</span></span> | <span data-ttu-id="fbb75-3278">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3278">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3279">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3279">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3280">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-3280">8</span></span> |
| <span data-ttu-id="fbb75-3281">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3281">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3282">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3282">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3283">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3283">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3284">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3284">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3285">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3285">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3286">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3286">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3287">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3287">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3288">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3288">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3289">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3289">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3290">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3290">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3291">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3292">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3293">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3294">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3294">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3295">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3296">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3296">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3297">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3297">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3298">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3299">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3299">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3300">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3300">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3301">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3301">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3302">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3302">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3303">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3303">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3304">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3304">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3305">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3305">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3306">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3306">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3307">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3307">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3308">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3308">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3309">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3309">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3310">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3310">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3311">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3311">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3312">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3312">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3313">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3313">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3314">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3314">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3315">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3315">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3316">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3316">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3317">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3317">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3318">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3318">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3319">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3319">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3320">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3320">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3321">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3321">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3322">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3322">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3323">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3323">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3324">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3324">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3325">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3325">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="fbb75-3326">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3326">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="fbb75-3327">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3327">Target</span></span> | <span data-ttu-id="fbb75-3328">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3328">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3329">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3329">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3330">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-3330">8</span></span> |
| <span data-ttu-id="fbb75-3331">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3331">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3333">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3333">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3334">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3334">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3335">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3335">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3336">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3336">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3337">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3337">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3338">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3338">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3340">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3340">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3342">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3344">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3344">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3346">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3346">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3348">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3348">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3349">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3349">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3350">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3350">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3351">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3351">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3352">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3352">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3354">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3354">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3355">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3355">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3357">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3357">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3359">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3360">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3361">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3362">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3363">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3363">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3364">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3365">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3366">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3367">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3369">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3370">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3371">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3372">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3372">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3374">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3374">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3375">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3375">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3376">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3376">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3377">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3378">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3378">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3379">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3380">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3380">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3381">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3381">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3382">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3382">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3383">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3383">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3384">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3384">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3386">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3386">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="fbb75-3387">DXGI_FORMAT_R8 \_ uint<sup>FNS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3387">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="fbb75-3388">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3388">Target</span></span> | <span data-ttu-id="fbb75-3389">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3389">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3390">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3390">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3391">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-3391">8</span></span> |
| <span data-ttu-id="fbb75-3392">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3392">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3393">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3393">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3394">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3394">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3395">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3395">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3396">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3396">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3397">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3397">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3398">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3399">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3399">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3400">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3400">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3401">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3401">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3402">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3402">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3403">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3403">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3404">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3404">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3405">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3405">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3406">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3406">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3407">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3407">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3408">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3408">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3409">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3410">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3411">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3412">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3413">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3414">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3415">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3415">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3416">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3416">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3417">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3417">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3418">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3418">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3419">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3419">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3420">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3420">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3421">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3421">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3422">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3422">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3423">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3423">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3424">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3424">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3425">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3426">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3427">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3428">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3429">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3429">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3430">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3431">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3431">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3432">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3433">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3434">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3435">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3435">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3436">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="fbb75-3437">DXGI_FORMAT_R8 \_ ronfler<sup>FNS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3437">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="fbb75-3438">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3438">Target</span></span> | <span data-ttu-id="fbb75-3439">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3439">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3440">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3441">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-3441">8</span></span> |
| <span data-ttu-id="fbb75-3442">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3442">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3443">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3443">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3444">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3445">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3446">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3447">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3448">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3449">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3450">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3451">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3452">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3453">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3454">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3455">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3456">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3457">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3457">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3458">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3459">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3460">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3460">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3461">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3461">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3462">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3462">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3463">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3463">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3464">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3464">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3465">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3465">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3466">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3466">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3467">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3467">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3468">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3468">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3469">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3469">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3470">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3470">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3471">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3471">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3472">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3472">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3473">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3473">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3474">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3474">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3475">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3475">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3476">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3476">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3477">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3477">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3478">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3478">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3479">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3479">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3480">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3480">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3481">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3481">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3482">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3482">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3483">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3483">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3484">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3484">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3485">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3485">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3486">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3486">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="fbb75-3487">DXGI_FORMAT_R8 \_ Saint<sup>FNS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3487">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="fbb75-3488">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3488">Target</span></span> | <span data-ttu-id="fbb75-3489">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3489">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3490">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3490">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3491">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-3491">8</span></span> |
| <span data-ttu-id="fbb75-3492">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3492">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3493">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3493">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3494">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3495">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3496">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3497">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3498">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3499">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3499">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3500">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3501">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3501">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3502">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3502">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3503">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3503">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3504">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3504">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3505">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3505">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3506">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3506">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3507">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3507">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3508">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3508">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3509">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3509">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3510">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3510">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3511">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3511">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3512">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3512">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3513">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3513">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3514">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3514">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3515">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3515">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3516">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3516">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3517">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3517">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3518">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3518">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3519">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3519">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3520">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3520">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3521">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3521">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3522">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3522">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3523">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3523">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3524">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3524">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3525">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3525">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3526">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3526">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3527">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3527">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3528">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3528">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3529">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3529">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3530">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3530">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3531">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3531">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3532">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3532">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3533">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3533">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3534">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3534">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3535">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3535">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3536">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3536">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="fbb75-3537">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3537">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="fbb75-3538">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3538">Target</span></span> | <span data-ttu-id="fbb75-3539">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3539">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3540">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3540">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3541">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-3541">8</span></span> |
| <span data-ttu-id="fbb75-3542">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3542">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3544">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3544">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3545">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3545">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3546">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3546">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3547">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3547">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3548">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3548">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3549">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3549">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3551">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3551">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3552">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3552">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3553">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3553">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3555">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3555">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3557">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3558">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3559">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3559">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3560">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3561">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3561">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3562">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3563">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3565">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3565">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3567">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3567">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3568">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3568">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3569">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3569">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3570">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3570">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3571">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3571">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3572">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3572">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3573">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3573">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3574">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3575">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3576">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3577">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3578">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3578">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3579">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3579">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3580">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3580">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3582">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3582">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3583">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3583">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3584">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3585">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3586">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3586">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3587">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3588">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3589">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3590">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3591">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3592">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3592">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3594">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="fbb75-3595">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3595">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="fbb75-3596">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3596">Target</span></span> | <span data-ttu-id="fbb75-3597">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3597">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3598">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3599">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-3599">32</span></span> |
| <span data-ttu-id="fbb75-3600">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3600">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3601">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3601">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3602">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3602">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3603">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3603">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3604">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3604">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3605">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3605">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3606">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3607">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3607">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3608">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3608">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3609">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3609">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3610">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3610">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3611">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3612">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3613">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3613">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3614">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3615">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3615">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3616">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3617">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3618">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3618">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3619">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3619">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3620">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3620">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3621">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3621">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3622">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3622">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3623">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3623">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3624">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3624">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3625">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3625">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3626">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3626">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3627">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3627">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3628">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3628">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3629">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3629">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3630">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3630">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3631">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3631">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3632">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3632">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3633">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3633">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3634">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3634">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3635">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3635">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3636">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3636">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3637">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3637">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3638">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3638">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3639">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3639">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3640">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3640">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3641">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3641">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3642">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3642">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3643">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3643">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3644">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3644">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="fbb75-3645">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3645">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="fbb75-3646">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3646">Target</span></span> | <span data-ttu-id="fbb75-3647">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3647">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3648">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3648">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3649">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-3649">16</span></span> |
| <span data-ttu-id="fbb75-3650">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3650">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3651">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3651">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3652">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3652">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3653">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3653">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3654">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3654">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3655">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3655">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3656">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3657">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3658">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3659">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3659">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3660">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3660">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3661">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3661">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3662">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3662">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3663">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3663">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3664">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3664">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3665">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3665">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3666">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3666">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3667">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3667">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3668">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3668">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3669">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3669">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3670">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3670">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3671">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3671">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3672">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3672">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3673">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3673">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3674">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3674">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3675">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3675">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3676">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3676">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3677">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3677">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3678">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3678">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3679">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3679">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3680">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3680">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3681">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3681">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3682">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3682">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3683">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3684">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3685">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3686">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3687">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3687">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3688">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3688">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3689">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3689">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3690">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3690">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3691">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3691">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3692">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3692">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3693">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3693">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3694">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="fbb75-3695">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3695">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="fbb75-3696">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3696">Target</span></span> | <span data-ttu-id="fbb75-3697">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3697">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3698">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3699">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-3699">16</span></span> |
| <span data-ttu-id="fbb75-3700">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3700">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3701">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3701">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3702">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3702">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3703">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3703">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3704">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3704">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3705">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3705">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3706">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3706">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3707">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3707">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3708">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3708">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3709">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3709">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3710">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3711">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3712">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3713">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3713">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3714">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3715">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3715">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3716">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3716">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3717">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3718">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3719">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3720">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3721">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3722">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3723">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3723">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3724">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3725">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3726">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3727">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3728">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3729">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3730">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3730">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3731">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3731">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3732">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3732">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3733">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3733">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3734">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3734">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3735">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3735">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3736">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3736">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3737">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3737">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3738">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3738">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3739">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3739">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3740">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3741">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3741">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3742">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3742">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3743">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3743">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3744">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3744">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="fbb75-3745">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non typé (70)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3745">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="fbb75-3746">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3746">Target</span></span> | <span data-ttu-id="fbb75-3747">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3747">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3748">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3748">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3749">4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3749">4</span></span> |
| <span data-ttu-id="fbb75-3750">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3750">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3751">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3751">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3752">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3752">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3753">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3753">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3754">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3754">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3755">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3755">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3756">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3756">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3757">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3758">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3758">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3759">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3759">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3760">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3760">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3761">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3761">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3762">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3762">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3763">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3763">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3764">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3764">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3765">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3765">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3766">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3766">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3767">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3767">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3768">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3768">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3769">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3769">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3770">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3770">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3771">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3771">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3772">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3772">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3773">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3773">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3774">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3774">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3775">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3775">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3776">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3776">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3777">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3777">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3778">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3778">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3779">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3779">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3780">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3780">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3781">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3781">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3782">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3782">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3783">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3783">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3784">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3784">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3785">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3785">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3786">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3786">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3787">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3787">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3788">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3788">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3789">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3789">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3790">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3790">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3791">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3791">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3792">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3792">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3793">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3793">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3794">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3794">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="fbb75-3795">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3795">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="fbb75-3796">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3796">Target</span></span> | <span data-ttu-id="fbb75-3797">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3797">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3798">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3798">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3799">4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3799">4</span></span> |
| <span data-ttu-id="fbb75-3800">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3800">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3802">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3802">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3803">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3803">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3804">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3805">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3806">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3807">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3810">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3812">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3812">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3814">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3814">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3816">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3816">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3817">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3817">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3818">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3818">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3819">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3819">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3820">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3820">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3822">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3822">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3823">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3823">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3824">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3824">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3825">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3825">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3826">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3826">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3827">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3827">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3828">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3828">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3829">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3829">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3830">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3830">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3831">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3831">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3832">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3832">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3833">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3833">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3834">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3834">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3835">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3835">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3836">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3836">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3837">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3837">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3838">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3838">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3840">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3841">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3842">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3843">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3844">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3845">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3846">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3847">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3848">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3849">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3850">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3850">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3852">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3852">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="fbb75-3853">DXGI_FORMAT_BC1 \_ UNORM \_ sRVB<sup>FNC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3853">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="fbb75-3854">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3854">Target</span></span> | <span data-ttu-id="fbb75-3855">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3855">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3856">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3856">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3857">4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3857">4</span></span> |
| <span data-ttu-id="fbb75-3858">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3858">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3860">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3860">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3861">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3861">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3862">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3862">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3863">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3863">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3864">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3864">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3865">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3865">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3867">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3867">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3868">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3870">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3870">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3872">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3872">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3874">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3874">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3875">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3875">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3876">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3876">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3877">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3877">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3878">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3878">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3880">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3881">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3882">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3883">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3884">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3885">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3886">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3887">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3887">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3888">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3889">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3890">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3891">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3893">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3894">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3895">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3896">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3896">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3898">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3898">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3899">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3899">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3900">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3900">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3901">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3901">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3902">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3902">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3903">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3903">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3904">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3904">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3905">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3906">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3907">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3908">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3908">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3910">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3910">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="fbb75-3911">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non typé (73)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3911">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="fbb75-3912">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3912">Target</span></span> | <span data-ttu-id="fbb75-3913">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3913">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3914">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3914">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3915">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-3915">8</span></span> |
| <span data-ttu-id="fbb75-3916">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3916">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-3917">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3917">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3918">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3918">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3919">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3919">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3920">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3920">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3921">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3921">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3922">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3922">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-3923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3923">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3924">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-3925">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3925">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-3926">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3926">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3927">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3927">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3928">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3928">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3929">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3929">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3930">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3930">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3931">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3931">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-3932">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3932">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3933">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3933">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3934">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3934">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3935">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3935">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3936">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3936">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3937">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3937">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3938">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3938">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3939">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3939">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3940">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3940">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3941">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3941">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3942">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3942">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3943">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3943">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-3944">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-3944">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-3945">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3945">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-3946">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3946">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3947">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-3947">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-3948">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3948">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-3949">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-3949">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3950">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3950">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3951">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-3951">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-3952">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-3952">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-3953">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-3953">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-3954">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-3954">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-3955">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-3955">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-3956">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3956">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-3957">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3957">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-3958">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-3958">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-3959">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3959">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-3960">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-3960">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="fbb75-3961">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3961">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="fbb75-3962">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-3962">Target</span></span> | <span data-ttu-id="fbb75-3963">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-3963">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-3964">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3964">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-3965">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-3965">8</span></span> |
| <span data-ttu-id="fbb75-3966">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-3966">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3968">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-3968">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3969">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3969">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3970">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-3970">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3971">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-3971">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-3972">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3972">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-3973">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3973">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3975">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-3975">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-3976">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-3976">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3978">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3978">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3980">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3980">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3982">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3982">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3983">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-3983">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-3984">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-3984">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-3985">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-3985">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-3986">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-3986">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-3988">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-3988">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-3989">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-3989">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3990">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-3990">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-3991">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-3991">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-3992">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-3992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-3993">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-3993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3994">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-3994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-3995">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-3995">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-3996">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-3997">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-3998">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-3998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-3999">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-3999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4000">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4001">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4002">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4003">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4004">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4004">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4006">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4007">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4008">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4009">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4010">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4010">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4011">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4012">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4013">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4014">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4015">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4016">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4016">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4018">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4018">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="fbb75-4019">DXGI_FORMAT_BC2 \_ UNORM \_ sRVB<sup>FNC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4019">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="fbb75-4020">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4020">Target</span></span> | <span data-ttu-id="fbb75-4021">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4021">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4022">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4022">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4023">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-4023">8</span></span> |
| <span data-ttu-id="fbb75-4024">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4024">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4026">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4026">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4027">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4027">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4028">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4029">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4029">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4030">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4030">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4031">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4031">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4033">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4033">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4034">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4034">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4036">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4036">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4038">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4038">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4040">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4040">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4041">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4041">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4042">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4042">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4043">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4043">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4044">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4044">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4046">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4046">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4047">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4047">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4048">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4048">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4049">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4049">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4050">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4050">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4051">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4051">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4052">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4052">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4053">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4053">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4054">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4054">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4055">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4055">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4056">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4057">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4058">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4059">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4060">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4060">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4061">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4061">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4062">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4062">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4064">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4064">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4065">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4065">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4066">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4066">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4067">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4067">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4068">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4068">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4069">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4069">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4070">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4070">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4071">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4072">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4072">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4073">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4073">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4074">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4074">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4076">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="fbb75-4077">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non typé (76)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4077">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="fbb75-4078">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4078">Target</span></span> | <span data-ttu-id="fbb75-4079">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4079">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4080">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4081">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-4081">8</span></span> |
| <span data-ttu-id="fbb75-4082">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4082">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-4083">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4083">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4084">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4085">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4086">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4087">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4088">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-4089">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4089">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4090">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4090">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-4091">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4091">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-4092">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4092">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4093">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4093">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4094">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4094">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4095">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4095">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4096">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4096">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4097">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4097">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-4098">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4098">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4099">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4100">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4101">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4102">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4103">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4104">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4105">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4105">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4106">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4107">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4108">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4109">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4110">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4111">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4112">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4112">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4113">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4113">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4114">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4114">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-4115">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4116">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4117">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4118">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4119">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4119">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4120">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4121">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4122">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4122">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4123">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4123">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4124">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4124">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4125">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4125">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4126">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4126">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="fbb75-4127">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4127">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="fbb75-4128">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4128">Target</span></span> | <span data-ttu-id="fbb75-4129">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4129">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4130">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4131">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-4131">8</span></span> |
| <span data-ttu-id="fbb75-4132">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4132">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4134">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4134">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4135">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4135">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4136">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4136">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4137">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4137">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4138">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4139">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4139">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4141">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4142">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4142">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4144">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4144">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4146">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4146">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4148">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4148">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4149">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4149">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4150">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4150">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4151">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4151">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4152">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4152">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4154">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4154">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4155">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4155">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4156">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4156">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4157">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4157">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4158">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4158">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4159">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4159">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4160">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4160">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4161">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4161">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4162">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4162">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4163">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4163">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4164">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4164">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4165">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4165">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4166">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4166">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4167">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4167">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4168">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4168">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4169">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4169">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4170">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4170">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4172">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4172">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4173">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4173">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4174">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4174">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4175">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4175">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4176">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4176">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4177">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4177">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4178">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4178">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4179">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4179">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4180">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4180">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4181">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4181">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4182">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4182">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4184">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4184">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="fbb75-4185">DXGI_FORMAT_BC3 \_ UNORM \_ sRVB<sup>FNC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4185">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="fbb75-4186">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4186">Target</span></span> | <span data-ttu-id="fbb75-4187">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4187">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4188">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4188">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4189">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-4189">8</span></span> |
| <span data-ttu-id="fbb75-4190">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4190">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4192">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4192">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4193">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4193">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4194">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4194">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4195">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4195">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4196">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4196">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4197">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4197">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4199">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4199">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4200">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4202">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4202">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4204">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4204">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4206">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4207">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4208">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4209">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4210">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4210">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4212">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4213">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4214">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4215">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4216">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4217">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4218">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4219">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4219">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4220">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4221">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4222">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4223">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4225">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4226">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4227">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4228">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4228">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4230">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4230">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4231">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4231">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4232">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4232">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4233">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4233">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4234">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4234">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4235">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4235">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4236">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4236">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4237">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4237">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4238">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4238">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4239">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4239">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4240">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4240">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4242">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4242">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="fbb75-4243">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non typé (79)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4243">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="fbb75-4244">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4244">Target</span></span> | <span data-ttu-id="fbb75-4245">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4245">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4246">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4246">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4247">4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4247">4</span></span> |
| <span data-ttu-id="fbb75-4248">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4248">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4249">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4250">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4250">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4251">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4251">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4252">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4252">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4253">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4253">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4254">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-4255">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4255">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4256">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4256">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-4257">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4257">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-4258">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4258">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4259">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4260">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4261">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4261">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4262">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4263">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4263">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-4264">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4264">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4265">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4265">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4266">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4266">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4267">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4267">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4268">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4268">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4269">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4269">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4270">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4270">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4271">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4271">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4272">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4272">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4273">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4273">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4274">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4274">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4275">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4275">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4276">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4276">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4277">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4277">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4278">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4278">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4279">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4279">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4280">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4280">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-4281">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4281">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4282">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4282">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4283">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4283">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4284">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4284">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4285">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4285">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4286">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4286">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4287">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4287">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4288">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4289">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4290">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4291">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4291">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4292">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="fbb75-4293">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4293">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="fbb75-4294">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4294">Target</span></span> | <span data-ttu-id="fbb75-4295">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4295">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4296">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4297">4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4297">4</span></span> |
| <span data-ttu-id="fbb75-4298">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4298">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4299">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4300">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4301">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4302">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4304">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-4305">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4305">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4306">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4306">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-4307">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4307">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-4308">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4308">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4309">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4309">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4310">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4310">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4311">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4311">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4312">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4312">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4313">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4313">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-4314">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4314">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4315">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4315">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4316">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4316">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4317">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4317">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4318">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4318">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4319">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4319">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4320">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4320">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4321">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4321">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4322">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4322">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4323">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4323">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4324">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4324">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4325">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4325">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4326">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4326">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4327">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4327">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4328">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4328">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4329">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4329">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4330">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4330">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-4331">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4332">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4333">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4334">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4335">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4335">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4336">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4337">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4337">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4338">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4338">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4339">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4339">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4340">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4340">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4341">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4341">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4342">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4342">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="fbb75-4343">DXGI_FORMAT_BC4 \_ ronfler<sup>FNC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4343">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="fbb75-4344">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4344">Target</span></span> | <span data-ttu-id="fbb75-4345">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4345">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4346">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4346">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4347">4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4347">4</span></span> |
| <span data-ttu-id="fbb75-4348">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4348">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-4349">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4349">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4350">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4350">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4351">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4352">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4353">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4354">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4354">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-4355">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4355">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4356">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4356">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-4357">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4357">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-4358">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4358">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4359">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4359">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4360">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4360">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4361">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4361">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4362">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4362">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4363">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4363">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-4364">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4364">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4365">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4365">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4366">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4366">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4367">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4367">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4368">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4368">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4369">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4369">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4370">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4370">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4371">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4371">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4372">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4372">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4373">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4373">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4374">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4374">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4375">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4375">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4376">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4376">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4377">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4377">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4378">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4378">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4379">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4379">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4380">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4380">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-4381">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4381">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4382">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4382">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4383">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4383">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4384">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4384">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4385">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4385">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4386">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4386">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4387">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4387">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4388">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4388">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4389">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4389">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4390">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4390">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4391">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4391">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4392">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4392">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="fbb75-4393">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non typé (82)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4393">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="fbb75-4394">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4394">Target</span></span> | <span data-ttu-id="fbb75-4395">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4395">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4396">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4396">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4397">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-4397">8</span></span> |
| <span data-ttu-id="fbb75-4398">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4398">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-4399">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4399">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4400">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4400">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4401">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4402">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4403">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4404">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-4405">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4405">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4406">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4406">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-4407">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4407">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-4408">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4408">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4409">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4409">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4410">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4410">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4411">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4411">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4412">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4412">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4413">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4413">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-4414">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4414">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4415">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4415">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4416">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4417">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4418">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4419">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4420">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4421">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4421">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4422">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4422">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4423">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4423">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4424">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4424">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4425">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4425">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4426">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4426">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4427">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4427">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4428">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4428">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4429">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4429">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4430">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4430">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-4431">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4431">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4432">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4432">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4433">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4433">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4434">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4434">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4435">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4435">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4436">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4437">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4438">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4439">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4440">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4441">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4441">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4442">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="fbb75-4443">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4443">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="fbb75-4444">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4444">Target</span></span> | <span data-ttu-id="fbb75-4445">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4445">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4446">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4447">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-4447">8</span></span> |
| <span data-ttu-id="fbb75-4448">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4448">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-4449">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4449">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4450">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4451">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4452">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4453">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4454">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4454">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-4455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4455">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4456">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4456">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-4457">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4457">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-4458">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4458">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4459">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4459">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4460">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4460">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4461">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4461">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4462">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4462">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4463">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4463">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-4464">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4464">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4465">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4465">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4466">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4466">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4467">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4467">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4468">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4468">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4469">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4470">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4471">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4471">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4472">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4473">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4474">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4475">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4476">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4477">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4478">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4479">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4480">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4480">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-4481">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4481">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4482">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4482">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4483">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4483">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4484">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4484">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4485">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4485">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4486">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4486">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4487">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4487">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4488">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4488">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4489">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4489">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4490">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4490">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4491">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4491">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4492">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4492">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="fbb75-4493">DXGI_FORMAT_BC5 \_ ronfler<sup>FNC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4493">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="fbb75-4494">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4494">Target</span></span> | <span data-ttu-id="fbb75-4495">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4495">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4496">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4496">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4497">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-4497">8</span></span> |
| <span data-ttu-id="fbb75-4498">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4498">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-4499">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4499">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4500">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4500">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4501">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4501">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4502">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4502">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4503">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4503">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4504">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4504">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-4505">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4505">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4506">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-4507">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4507">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-4508">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4508">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4509">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4509">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4510">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4510">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4511">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4511">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4512">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4512">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4513">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4513">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-4514">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4515">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4516">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4517">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4518">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4519">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4520">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4521">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4521">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4522">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4523">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4524">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4525">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4526">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4527">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4528">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4529">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4530">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4530">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-4531">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4531">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4532">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4532">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4533">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4533">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4534">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4534">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4535">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4535">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4536">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4536">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4537">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4537">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4538">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4538">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4539">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4539">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4540">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4540">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4541">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4541">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4542">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="fbb75-4543">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4543">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="fbb75-4544">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4544">Target</span></span> | <span data-ttu-id="fbb75-4545">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4546">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4547">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-4547">16</span></span> |
| <span data-ttu-id="fbb75-4548">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4548">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4550">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4551">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4552">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4553">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4554">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4555">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4555">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4557">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4558">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4560">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4560">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4562">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4562">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4564">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4564">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4565">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4565">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4566">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4566">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4567">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4567">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4568">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4568">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4570">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4570">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4572">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4574">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4574">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4576">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4577">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4578">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4579">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4580">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4580">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4581">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4582">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4583">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4584">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4585">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4586">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4587">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4588">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4589">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4589">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4591">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4591">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4593">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4593">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4595">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4595">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4597">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4597">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4599">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4599">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4600">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4600">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4601">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4601">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4602">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4602">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4603">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4603">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4604">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4604">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4605">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4605">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4606">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4606">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="fbb75-4607">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4607">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="fbb75-4608">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4608">Target</span></span> | <span data-ttu-id="fbb75-4609">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4609">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4610">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4610">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4611">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-4611">16</span></span> |
| <span data-ttu-id="fbb75-4612">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4612">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4614">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4614">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4615">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4615">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4616">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4616">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4617">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4617">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4618">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4618">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4619">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4621">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4622">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4622">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4624">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4624">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4626">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4626">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4628">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4628">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4629">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4629">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4630">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4630">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4631">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4631">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4632">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4632">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4634">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4634">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4635">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4635">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4636">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4636">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4637">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4637">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4638">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4638">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4639">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4639">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4640">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4640">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4641">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4641">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4642">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4642">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4643">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4643">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4644">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4644">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4645">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4645">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4646">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4646">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4647">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4647">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4648">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4648">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4649">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4649">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4650">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4650">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4652">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4652">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4653">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4653">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4654">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4654">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4655">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4655">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4656">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4656">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4657">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4658">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4658">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4659">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4659">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4660">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4660">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4661">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4661">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4662">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4662">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4663">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="fbb75-4664">\_<sup>PC</sup> DXGI_FORMAT_B8G8R8A8 type (90)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4664">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="fbb75-4665">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4665">Target</span></span> | <span data-ttu-id="fbb75-4666">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4666">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4667">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4668">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-4668">32</span></span> |
| <span data-ttu-id="fbb75-4669">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4669">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-4670">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4670">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4671">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4672">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4673">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4674">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4675">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4675">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4676">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4677">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4677">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-4678">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4678">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-4679">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4679">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4680">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4681">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4682">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4682">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4683">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4684">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4684">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-4685">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4685">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4686">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4686">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4687">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4687">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4688">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4688">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4689">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4689">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4690">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4690">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4691">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4691">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4692">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4692">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4693">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4693">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4694">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4694">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4695">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4695">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4696">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4696">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4697">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4697">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4698">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4698">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4699">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4699">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4700">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4700">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4701">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4701">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-4702">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4702">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4703">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4703">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4704">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4704">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4705">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4705">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4706">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4707">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4708">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4709">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4710">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4711">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4712">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4713">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="fbb75-4714">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4714">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="fbb75-4715">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4715">Target</span></span> | <span data-ttu-id="fbb75-4716">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4717">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4718">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-4718">32</span></span> |
| <span data-ttu-id="fbb75-4719">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4719">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4721">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4722">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4723">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4724">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4726">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4728">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4730">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4732">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4732">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4734">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4734">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4736">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4737">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4738">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4738">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4739">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4740">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4740">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4742">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4742">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4744">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4746">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4746">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4748">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4749">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4750">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4751">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4752">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4752">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4753">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4754">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4755">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4756">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4757">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4758">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4759">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4760">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4761">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4761">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4763">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4763">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4765">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4765">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4767">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4767">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4769">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4769">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4771">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4771">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4772">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4772">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4774">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4774">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4775">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4775">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4776">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4776">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4778">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4778">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4780">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4780">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4782">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="fbb75-4783">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRVB<sup>FNS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4783">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="fbb75-4784">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4784">Target</span></span> | <span data-ttu-id="fbb75-4785">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4785">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4786">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4787">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-4787">32</span></span> |
| <span data-ttu-id="fbb75-4788">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4788">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4790">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4790">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4791">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4791">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4792">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4792">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4793">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4793">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4794">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4794">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4795">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4797">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4799">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4799">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4801">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4801">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4803">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4803">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4805">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4805">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4806">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4806">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4807">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4807">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4808">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4808">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4809">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4809">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4811">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4811">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4813">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4815">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4815">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4817">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4817">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4818">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4818">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4819">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4819">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4820">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4820">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4821">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4821">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4822">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4822">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4823">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4823">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4824">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4824">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4825">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4825">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4826">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4826">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4827">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4827">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4828">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4828">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4829">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4829">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4830">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4830">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4832">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4832">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4834">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4834">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4836">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4836">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4838">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4838">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4840">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4840">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4841">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4841">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4843">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4843">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4844">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4844">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4845">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4845">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4847">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4847">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4849">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4849">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4851">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="fbb75-4852">\_<sup>PC</sup> DXGI_FORMAT_B8G8R8X8 type (92)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4852">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="fbb75-4853">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4853">Target</span></span> | <span data-ttu-id="fbb75-4854">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4854">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4855">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4856">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-4856">32</span></span> |
| <span data-ttu-id="fbb75-4857">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4857">Format Support</span></span> | \- |
| <span data-ttu-id="fbb75-4858">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4858">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4859">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4860">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4861">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4862">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4863">Texture2D</span></span> | \- |
| <span data-ttu-id="fbb75-4864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4864">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-4865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4865">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-4866">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-4867">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4868">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4869">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4870">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4870">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4871">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4872">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4872">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-4873">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-4874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4874">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4875">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4876">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4877">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4878">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4879">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4880">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4880">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4881">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4882">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4884">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4886">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4887">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4888">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4889">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-4890">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4891">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-4892">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-4893">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-4894">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4894">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4895">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4896">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4897">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4898">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-4899">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-4900">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4900">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-4901">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="fbb75-4902">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4902">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="fbb75-4903">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4903">Target</span></span> | <span data-ttu-id="fbb75-4904">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4904">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4905">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4906">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-4906">32</span></span> |
| <span data-ttu-id="fbb75-4907">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4907">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4909">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4909">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4910">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4911">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4912">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4913">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4914">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4916">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4918">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4918">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4920">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4920">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4922">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4922">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4924">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4924">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4925">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4925">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4926">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4926">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4927">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4927">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4928">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4928">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4930">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4930">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4932">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4932">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4934">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4934">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4936">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-4936">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-4937">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-4937">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-4938">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-4938">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4939">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-4939">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-4940">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-4940">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-4941">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4941">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-4942">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4942">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-4943">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-4943">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-4944">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4944">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-4945">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-4945">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-4946">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4946">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-4947">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-4947">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4948">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-4948">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-4949">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-4949">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4951">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-4951">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4953">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-4953">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4955">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-4955">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4957">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-4957">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4959">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-4959">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-4960">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-4960">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-4961">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-4961">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-4962">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4962">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-4963">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4963">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4965">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-4965">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-4967">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4967">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4969">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-4969">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="fbb75-4970">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRVB<sup>FNS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4970">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="fbb75-4971">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-4971">Target</span></span> | <span data-ttu-id="fbb75-4972">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-4972">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-4973">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4973">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-4974">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-4974">32</span></span> |
| <span data-ttu-id="fbb75-4975">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-4975">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4977">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-4977">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4978">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4978">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4979">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-4979">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4980">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-4980">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-4981">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4981">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-4982">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4982">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4984">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-4984">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4986">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-4986">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4988">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4988">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4990">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4990">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4992">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4992">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4993">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-4993">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-4994">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-4994">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-4995">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-4995">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-4996">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-4996">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-4998">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-4998">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5000">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5000">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5002">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5002">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5004">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5004">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5005">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5005">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5006">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5006">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5007">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5007">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5008">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5008">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5009">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5009">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5010">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5010">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5011">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5011">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5012">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5012">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5013">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5013">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5014">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5014">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5015">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5015">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5016">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5016">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5017">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5017">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5019">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5019">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5021">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5021">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5023">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5023">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5025">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5025">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5027">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5027">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5028">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5028">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5029">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5029">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5030">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5030">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-5031">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5031">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-5032">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5032">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-5033">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5033">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5035">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5035">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="fbb75-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="fbb75-5037">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5037">Target</span></span> | <span data-ttu-id="fbb75-5038">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5038">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5039">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5039">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5040">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-5040">32</span></span> |
| <span data-ttu-id="fbb75-5041">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5041">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5043">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5043">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5044">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5044">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5045">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5045">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5046">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5046">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5047">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5047">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5048">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5050">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5051">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5052">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5053">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5054">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5055">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5056">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5056">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5057">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5058">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5058">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5059">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5060">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5061">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5062">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5063">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5064">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5065">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5066">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5066">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5067">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5068">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5069">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5070">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5071">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5072">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5073">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5074">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5075">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5075">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5077">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5078">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5079">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5080">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5081">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5081">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5082">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5083">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5084">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5084">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5086">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5086">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5088">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5088">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5090">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5090">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5091">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="fbb75-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="fbb75-5093">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5093">Target</span></span> | <span data-ttu-id="fbb75-5094">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5094">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5095">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5096">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-5096">32</span></span> |
| <span data-ttu-id="fbb75-5097">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5097">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5099">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5099">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5100">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5101">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5102">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5103">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5104">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5106">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5107">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5107">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5108">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5108">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5109">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5109">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5110">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5110">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5111">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5111">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5112">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5112">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5113">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5113">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5114">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5114">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5115">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5115">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5116">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5116">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5117">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5117">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5118">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5118">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5119">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5119">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5120">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5120">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5121">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5121">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5122">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5122">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5123">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5123">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5124">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5124">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5125">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5125">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5126">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5126">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5127">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5127">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5128">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5128">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5129">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5129">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5130">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5130">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5131">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5131">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5133">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5133">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5134">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5134">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5135">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5135">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5136">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5136">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5137">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5137">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5138">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5138">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5139">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5139">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5140">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5140">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5142">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5142">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5144">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5144">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5146">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5146">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5147">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="fbb75-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="fbb75-5149">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5149">Target</span></span> | <span data-ttu-id="fbb75-5150">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5150">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5151">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5152">64</span><span class="sxs-lookup"><span data-stu-id="fbb75-5152">64</span></span> |
| <span data-ttu-id="fbb75-5153">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5153">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5155">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5155">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5156">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5157">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5158">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5159">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5160">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5162">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5163">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5164">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5164">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5165">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5165">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5166">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5166">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5167">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5167">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5168">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5168">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5169">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5169">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5170">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5170">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5171">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5171">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5172">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5172">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5173">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5173">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5174">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5174">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5175">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5175">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5176">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5176">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5177">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5177">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5178">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5178">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5179">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5179">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5180">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5180">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5181">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5181">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5182">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5182">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5183">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5183">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5184">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5184">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5185">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5185">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5186">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5186">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5187">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5187">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5189">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5189">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5190">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5190">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5191">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5191">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5192">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5192">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5193">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5193">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5194">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5194">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5195">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5195">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5196">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5196">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5198">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5198">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5200">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5200">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5202">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5202">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5203">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5203">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="fbb75-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="fbb75-5205">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5205">Target</span></span> | <span data-ttu-id="fbb75-5206">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5206">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5207">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5207">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5208">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-5208">8</span></span> |
| <span data-ttu-id="fbb75-5209">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5209">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5211">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5211">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5212">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5212">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5213">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5213">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5214">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5214">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5215">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5215">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5216">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5218">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5219">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5220">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5220">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5221">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5221">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5222">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5222">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5223">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5223">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5224">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5224">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5225">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5226">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5226">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5227">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5227">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5228">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5228">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5229">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5229">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5230">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5230">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5231">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5231">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5232">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5232">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5233">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5233">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5234">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5234">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5235">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5235">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5236">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5237">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5238">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5239">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5240">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5241">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5241">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5242">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5242">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5243">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5243">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5245">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5246">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5247">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5248">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5249">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5249">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5250">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5251">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5252">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5252">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5254">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5254">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5256">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5256">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5258">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5258">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5259">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5259">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="fbb75-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="fbb75-5261">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5261">Target</span></span> | <span data-ttu-id="fbb75-5262">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5262">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5263">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5263">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5264">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-5264">16</span></span> |
| <span data-ttu-id="fbb75-5265">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5265">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5267">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5267">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5268">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5268">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5269">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5269">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5270">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5270">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5271">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5271">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5272">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5272">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5274">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5274">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5275">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5275">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5276">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5276">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5277">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5277">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5278">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5278">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5279">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5279">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5280">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5280">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5281">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5281">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5282">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5282">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5283">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5283">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5284">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5284">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5285">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5286">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5286">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5287">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5287">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5288">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5288">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5289">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5289">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5290">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5290">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5291">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5291">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5292">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5292">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5293">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5293">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5294">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5294">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5295">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5295">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5296">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5296">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5297">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5297">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5298">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5298">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5299">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5299">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5301">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5301">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5302">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5302">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5303">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5303">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5304">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5304">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5305">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5305">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5306">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5306">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5307">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5307">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5308">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5308">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5310">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5310">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5312">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5312">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5314">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5314">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5315">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5315">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="fbb75-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="fbb75-5317">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5317">Target</span></span> | <span data-ttu-id="fbb75-5318">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5318">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5319">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5320">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-5320">16</span></span> |
| <span data-ttu-id="fbb75-5321">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5321">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5323">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5323">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5324">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5324">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5325">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5325">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5326">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5326">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5327">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5328">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5330">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5331">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5331">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5332">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5332">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5333">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5334">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5334">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5335">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5335">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5336">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5336">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5337">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5337">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5338">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5338">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5339">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5341">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5342">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5343">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5344">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5345">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5346">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5347">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5348">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5349">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5350">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5351">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5352">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5353">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5354">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5355">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5355">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5357">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5358">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5359">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5360">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5361">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5362">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5363">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5364">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5364">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5366">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5366">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5368">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5368">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5370">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5370">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5371">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5371">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="fbb75-5372">DXGI_FORMAT_420 \_ <sup>V</sup> opaque (106)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5372">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="fbb75-5373">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5373">Target</span></span> | <span data-ttu-id="fbb75-5374">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5374">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5375">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5375">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5376">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-5376">8</span></span> |
| <span data-ttu-id="fbb75-5377">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5377">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5379">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5379">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5380">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5381">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5382">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5383">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5384">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5386">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5386">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5387">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5387">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5388">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5388">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5389">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5389">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5390">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5390">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5391">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5391">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5392">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5392">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5393">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5393">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5394">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5394">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5395">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5395">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5396">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5396">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5397">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5397">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5398">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5398">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5399">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5399">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5400">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5400">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5401">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5401">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5402">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5402">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5403">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5403">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5404">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5404">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5405">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5405">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5406">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5406">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5407">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5407">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5408">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5408">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5409">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5409">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5410">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5410">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5411">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5411">CPU Lockable</span></span> | \- |
| <span data-ttu-id="fbb75-5412">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5412">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5413">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5413">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5414">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5414">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5415">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5415">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5416">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5416">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5417">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5417">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5418">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5418">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5419">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5419">Video Decoder Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5421">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5421">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5423">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5423">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5425">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5425">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5426">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5426">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="fbb75-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="fbb75-5428">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5428">Target</span></span> | <span data-ttu-id="fbb75-5429">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5429">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5430">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5430">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5431">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-5431">16</span></span> |
| <span data-ttu-id="fbb75-5432">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5432">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5434">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5434">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5435">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5435">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5436">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5436">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5437">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5437">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5438">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5438">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5439">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5439">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5441">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5441">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5442">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5442">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5443">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5443">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5444">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5444">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5445">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5445">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5446">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5446">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5447">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5447">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5448">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5448">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5449">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5449">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5450">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5450">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5451">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5451">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5452">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5452">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5453">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5454">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5455">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5456">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5457">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5457">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5458">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5459">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5460">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5461">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5462">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5463">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5464">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5465">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5466">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5466">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5468">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5468">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5469">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5469">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5470">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5470">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5471">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5471">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5472">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5472">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5473">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5474">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5474">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5475">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5475">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5477">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5477">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5479">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5479">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5481">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5481">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5482">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5482">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="fbb75-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="fbb75-5484">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5484">Target</span></span> | <span data-ttu-id="fbb75-5485">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5485">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5486">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5486">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5487">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-5487">32</span></span> |
| <span data-ttu-id="fbb75-5488">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5488">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5490">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5490">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5491">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5491">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5492">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5493">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5494">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5495">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5495">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5497">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5497">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5498">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5498">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5499">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5499">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5500">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5500">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5501">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5501">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5502">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5502">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5503">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5503">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5504">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5504">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5505">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5505">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5506">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5506">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5507">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5507">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5508">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5508">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5509">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5509">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5510">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5510">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5511">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5511">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5512">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5512">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5513">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5513">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5514">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5514">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5515">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5515">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5516">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5516">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5517">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5517">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5518">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5518">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5519">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5519">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5520">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5520">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5521">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5521">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5522">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5522">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5524">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5524">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5525">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5525">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5526">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5526">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5527">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5527">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5528">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5528">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5529">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5529">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5530">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5530">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5531">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5531">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5533">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5533">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5535">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5535">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5537">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5537">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5538">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5538">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="fbb75-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="fbb75-5540">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5540">Target</span></span> | <span data-ttu-id="fbb75-5541">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5541">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5542">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5542">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5543">32</span><span class="sxs-lookup"><span data-stu-id="fbb75-5543">32</span></span> |
| <span data-ttu-id="fbb75-5544">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5544">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5546">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5546">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5547">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5548">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5549">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5550">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5551">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5553">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5553">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5554">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5554">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5555">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5555">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5556">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5556">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5557">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5558">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5559">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5559">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5560">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5561">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5561">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5562">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5563">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5564">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5564">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5565">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5565">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5566">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5566">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5567">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5567">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5568">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5568">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5569">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5569">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5570">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5570">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5571">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5571">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5572">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5572">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5573">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5573">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5574">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5574">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5575">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5575">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5576">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5576">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5577">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5577">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5578">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5578">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5580">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5581">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5582">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5583">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5584">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5584">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5585">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5586">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5587">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5587">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5589">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5589">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5591">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5591">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5593">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5593">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5594">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="fbb75-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="fbb75-5596">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5596">Target</span></span> | <span data-ttu-id="fbb75-5597">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5597">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5598">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5599">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-5599">8</span></span> |
| <span data-ttu-id="fbb75-5600">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5600">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5602">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5602">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5603">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5604">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5605">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5606">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5607">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5609">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5610">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5611">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5612">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5613">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5614">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5615">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5615">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5616">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5617">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5617">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5618">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5619">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5620">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5621">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5622">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5622">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5623">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5623">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5624">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5624">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5625">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5625">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5626">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5626">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5627">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5627">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5628">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5628">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5629">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5629">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5630">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5630">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5631">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5631">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5632">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5632">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5633">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5633">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5634">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5634">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5636">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5636">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5637">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5637">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5638">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5638">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5639">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5639">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5640">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5640">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5641">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5641">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5642">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5642">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5643">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5643">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5645">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5645">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5647">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5647">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5649">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5649">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5650">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="fbb75-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="fbb75-5652">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5652">Target</span></span> | <span data-ttu-id="fbb75-5653">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5653">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5654">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5655">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-5655">8</span></span> |
| <span data-ttu-id="fbb75-5656">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5656">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5658">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5658">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5659">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5659">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5660">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5660">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5661">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5661">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5662">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5662">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5663">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5663">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5665">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5665">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5666">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5666">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5667">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5667">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5668">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5668">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5669">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5669">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5670">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5670">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5671">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5671">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5672">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5672">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5673">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5673">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5674">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5674">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5675">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5676">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5676">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5677">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5678">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5679">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5680">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5681">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5681">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5682">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5683">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5684">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5685">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5687">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5688">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5689">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5690">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5690">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5692">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5693">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5694">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5695">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5696">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5696">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5697">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5698">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5699">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-5700">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5700">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5702">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5702">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-5703">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5703">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5704">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5704">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="fbb75-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="fbb75-5706">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5706">Target</span></span> | <span data-ttu-id="fbb75-5707">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5707">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5708">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5708">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5709">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-5709">8</span></span> |
| <span data-ttu-id="fbb75-5710">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5710">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5712">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5712">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5713">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5713">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5714">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5714">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5715">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5715">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5716">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5716">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5717">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5717">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5719">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5719">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5720">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5721">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5721">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5722">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5722">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5723">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5723">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5724">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5724">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5725">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5725">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5726">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5726">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5727">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5727">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5728">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5729">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5730">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5731">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5732">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5733">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5734">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5735">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5735">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5736">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5737">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5738">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5739">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5740">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5741">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5742">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5743">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5744">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5744">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5746">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5747">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5748">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5749">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5750">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5750">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5751">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5752">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5752">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5753">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5753">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-5754">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5754">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5756">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-5757">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5757">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5758">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="fbb75-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="fbb75-5760">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5760">Target</span></span> | <span data-ttu-id="fbb75-5761">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5761">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5762">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5763">8</span><span class="sxs-lookup"><span data-stu-id="fbb75-5763">8</span></span> |
| <span data-ttu-id="fbb75-5764">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5764">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5766">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5766">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5767">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5768">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5769">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5770">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5771">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5771">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5773">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5773">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5774">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5774">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5775">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5775">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5776">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5776">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5777">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5777">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5778">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5778">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5779">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5779">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5780">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5780">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5781">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5781">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5782">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5783">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5784">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5784">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5785">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5785">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5786">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5786">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5787">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5787">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5788">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5788">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5789">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5789">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5790">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5790">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5791">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5791">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5792">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5792">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5793">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5793">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5794">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5794">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5795">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5795">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5796">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5796">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5797">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5797">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5798">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5798">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5800">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5801">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5802">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5803">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5804">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5804">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5805">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5806">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5807">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-5808">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5808">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5810">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5810">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-5811">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5811">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5812">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5812">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="fbb75-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="fbb75-5814">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5814">Target</span></span> | <span data-ttu-id="fbb75-5815">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5815">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5816">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5816">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5817">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-5817">16</span></span> |
| <span data-ttu-id="fbb75-5818">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5818">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="fbb75-5820">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5820">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5821">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5821">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5822">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5822">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5823">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5823">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5824">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5824">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5825">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5827">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5828">TextureCube</span></span> | \- |
| <span data-ttu-id="fbb75-5829">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5829">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="fbb75-5830">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5830">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5831">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5831">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5832">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5832">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5833">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5833">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5834">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5834">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5835">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5835">Mipmap</span></span> | \- |
| <span data-ttu-id="fbb75-5836">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5836">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5837">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5837">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5838">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5838">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5839">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5839">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5840">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5840">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5841">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5841">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5842">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5842">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5843">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5843">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5844">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5844">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5845">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5845">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5846">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5846">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5847">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5847">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5848">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5848">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5849">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5849">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5850">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5850">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5851">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5851">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5852">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5852">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5854">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5854">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5855">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5855">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5856">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5856">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5857">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5857">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5858">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5858">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5859">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5859">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5860">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5860">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5861">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5861">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-5862">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5862">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5864">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5864">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-5865">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5865">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5866">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5866">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="fbb75-5867">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5867">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="fbb75-5868">Cible</span><span class="sxs-lookup"><span data-stu-id="fbb75-5868">Target</span></span> | <span data-ttu-id="fbb75-5869">Support</span><span class="sxs-lookup"><span data-stu-id="fbb75-5869">Support</span></span> |
| - | - |
| <span data-ttu-id="fbb75-5870">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5870">Bits Per Element (BPE)</span></span> | <span data-ttu-id="fbb75-5871">16</span><span class="sxs-lookup"><span data-stu-id="fbb75-5871">16</span></span> |
| <span data-ttu-id="fbb75-5872">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="fbb75-5872">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5874">Buffer</span><span class="sxs-lookup"><span data-stu-id="fbb75-5874">Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5875">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5876">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5877">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="fbb75-5877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="fbb75-5878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5878">Texture1D</span></span> | \- |
| <span data-ttu-id="fbb75-5879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5879">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5881">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fbb75-5881">Texture3D</span></span> | \- |
| <span data-ttu-id="fbb75-5882">TextureCube</span><span class="sxs-lookup"><span data-stu-id="fbb75-5882">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5884">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5884">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5886">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5886">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5888">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5888">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5889">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="fbb75-5889">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="fbb75-5890">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="fbb75-5890">Shader gather4</span></span> | \- |
| <span data-ttu-id="fbb75-5891">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="fbb75-5891">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="fbb75-5892">MIP</span><span class="sxs-lookup"><span data-stu-id="fbb75-5892">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5894">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="fbb75-5894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="fbb75-5895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5895">RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5896">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5897">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="fbb75-5897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="fbb75-5898">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="fbb75-5898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="fbb75-5899">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="fbb75-5899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5900">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="fbb75-5900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="fbb75-5901">UAV typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5901">Typed UAV</span></span> | \- |
| <span data-ttu-id="fbb75-5902">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="fbb75-5903">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="fbb75-5904">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="fbb75-5904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="fbb75-5905">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="fbb75-5906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="fbb75-5906">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="fbb75-5907">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="fbb75-5908">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="fbb75-5908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5909">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="fbb75-5909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="fbb75-5910">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="fbb75-5910">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="fbb75-5912">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="fbb75-5912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5913">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="fbb75-5913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="fbb75-5914">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="fbb75-5914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="fbb75-5915">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="fbb75-5915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="fbb75-5916">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="fbb75-5916">Multisample Load</span></span> | \- |
| <span data-ttu-id="fbb75-5917">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="fbb75-5917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="fbb75-5918">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="fbb75-5918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="fbb75-5919">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="fbb75-5920">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5920">Video Processor Input</span></span> | \- |
| <span data-ttu-id="fbb75-5921">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5921">Video Processor Output</span></span> | \- |
| <span data-ttu-id="fbb75-5922">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="fbb75-5922">Shared Resource</span></span> | \- |
| <span data-ttu-id="fbb75-5923">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fbb75-5923">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="fbb75-5924">Mettre en forme les notes</span><span class="sxs-lookup"><span data-stu-id="fbb75-5924">Format notes</span></span>

<span data-ttu-id="fbb75-5925">L’objectif du format peut passer d’un niveau de fonctionnalité matériel à l’autre.</span><span class="sxs-lookup"><span data-stu-id="fbb75-5925">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="fbb75-5926"><sup>L</sup> : format non typé</span><span class="sxs-lookup"><span data-stu-id="fbb75-5926"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="fbb75-5927"><sup>PC</sup> : disposition partiellement typée, castable et simple</span><span class="sxs-lookup"><span data-stu-id="fbb75-5927"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="fbb75-5928"><sup>FCS</sup> : mise en page entièrement typée, castable et simple</span><span class="sxs-lookup"><span data-stu-id="fbb75-5928"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="fbb75-5929"><sup>FNS</sup> : mise en page entièrement typée, non stable et simple</span><span class="sxs-lookup"><span data-stu-id="fbb75-5929"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="fbb75-5930"><sup>PCC</sup> : disposition partiellement typée, castable et complexe</span><span class="sxs-lookup"><span data-stu-id="fbb75-5930"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="fbb75-5931"><sup>FCC</sup> : mise en page entièrement typée, castable et complexe</span><span class="sxs-lookup"><span data-stu-id="fbb75-5931"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="fbb75-5932"><sup>FNC</sup> : mise en page entièrement typée, non stable et complexe</span><span class="sxs-lookup"><span data-stu-id="fbb75-5932"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="fbb75-5933"><sup>V</sup> : format vidéo</span><span class="sxs-lookup"><span data-stu-id="fbb75-5933"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="fbb75-5934">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fbb75-5934">Related topics</span></span>

[<span data-ttu-id="fbb75-5935">Niveaux de fonctionnalité matérielle D3D12</span><span class="sxs-lookup"><span data-stu-id="fbb75-5935">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="fbb75-5936">[Implémentation de mémoires tampons secondaires pour le niveau de fonctionnalité Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="fbb75-5936">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="fbb75-5937">Mappage des formats hérités</span><span class="sxs-lookup"><span data-stu-id="fbb75-5937">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="fbb75-5938">Guide de programmation pour DXGI</span><span class="sxs-lookup"><span data-stu-id="fbb75-5938">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
