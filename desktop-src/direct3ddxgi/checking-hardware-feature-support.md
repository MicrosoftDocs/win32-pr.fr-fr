---
description: Cette section explique comment vérifier la prise en charge du format pour le matériel de niveau de fonctionnalité Direct3D à l’aide d’appels d’API.
ms.assetid: 0C40C73E-06F3-41FA-AA27-2C0B730B357B
title: Prise en charge de la fonctionnalité de vérification du matériel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b14f0de50c4236c4fce46ceda1896ee32721c3bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950207"
---
# <a name="checking-hardware-feature-support"></a><span data-ttu-id="71f8f-103">Prise en charge de la fonctionnalité de vérification du matériel</span><span class="sxs-lookup"><span data-stu-id="71f8f-103">Checking Hardware Feature Support</span></span>

<span data-ttu-id="71f8f-104">Cette section explique comment vérifier la prise en charge du format pour le matériel de niveau de fonctionnalité Direct3D à l’aide d’appels d’API.</span><span class="sxs-lookup"><span data-stu-id="71f8f-104">This section covers how to check on Format Support for Direct3D Feature Level Hardware using API calls.</span></span>

<span data-ttu-id="71f8f-105">Pour D3D11, utilisez [**ID3D11Device :: CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) pour vérifier par programme les informations dans les sections précédentes.</span><span class="sxs-lookup"><span data-stu-id="71f8f-105">For D3D11, use [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) to programmatically verify the info in the previous sections.</span></span> <span data-ttu-id="71f8f-106">Pour D3D12, utilisez [**ID3D12 :: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="71f8f-106">For D3D12 use [**ID3D12::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71f8f-107">Mettre en forme la cible</span><span class="sxs-lookup"><span data-stu-id="71f8f-107">Format target</span></span></th>
<th><span data-ttu-id="71f8f-108">D3D12</span><span class="sxs-lookup"><span data-stu-id="71f8f-108">D3D12</span></span></th>
<th><span data-ttu-id="71f8f-109">D3D11</span><span class="sxs-lookup"><span data-stu-id="71f8f-109">D3D11</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71f8f-110">Buffer</span><span class="sxs-lookup"><span data-stu-id="71f8f-110">Buffer</span></span></td>
<td><span data-ttu-id="71f8f-111">D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-111">D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-112">D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-112">D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-113">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="71f8f-113">Input Assembler Vertex Buffer</span></span></td>
<td><span data-ttu-id="71f8f-114">D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-114">D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-115">D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-115">D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-116">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="71f8f-116">Input Assembler Index Buffer</span></span></td>
<td><span data-ttu-id="71f8f-117">D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-117">D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-118">D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-118">D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-119">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="71f8f-119">Stream Output Buffer</span></span></td>
<td><span data-ttu-id="71f8f-120">D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-120">D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-121">D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-121">D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-122">Texture1D</span><span class="sxs-lookup"><span data-stu-id="71f8f-122">Texture1D</span></span></td>
<td><span data-ttu-id="71f8f-123">D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-123">D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-124">D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-124">D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-125">Texture2D</span><span class="sxs-lookup"><span data-stu-id="71f8f-125">Texture2D</span></span></td>
<td><span data-ttu-id="71f8f-126">D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-126">D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-127">D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-127">D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-128">Texture3D</span><span class="sxs-lookup"><span data-stu-id="71f8f-128">Texture3D</span></span></td>
<td><span data-ttu-id="71f8f-129">D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-129">D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-130">D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-130">D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="71f8f-131">TextureCube</span></span></td>
<td><span data-ttu-id="71f8f-132">D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-132">D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-133">D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-133">D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-134">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="71f8f-134">Shader ld</span></span></td>
<td><span data-ttu-id="71f8f-135">D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-135">D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-136">D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-136">D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-137">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="71f8f-137">Shader sample (any filter)</span></span></td>
<td><span data-ttu-id="71f8f-138">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-138">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-139">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-139">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-140">Sample_c du nuanceur (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="71f8f-140">Shader sample_c (comparison filter)</span></span></td>
<td><span data-ttu-id="71f8f-141">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-141">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-142">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-142">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-143">Exemple de nuanceur (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="71f8f-143">Shader sample (mono 1_bit_filter)</span></span></td>
<td><span data-ttu-id="71f8f-144">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-144">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-145">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-145">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-146">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="71f8f-146">Shader gather4</span></span></td>
<td><span data-ttu-id="71f8f-147">D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-147">D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-148">D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-148">D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-149">Gather4_c de nuanceur</span><span class="sxs-lookup"><span data-stu-id="71f8f-149">Shader gather4_c</span></span></td>
<td><span data-ttu-id="71f8f-150">D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-150">D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-151">D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-151">D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-152">MIP</span><span class="sxs-lookup"><span data-stu-id="71f8f-152">Mipmap</span></span></td>
<td><span data-ttu-id="71f8f-153">D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-153">D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-154">D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-154">D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-155">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="71f8f-155">Mipmap Auto-Generation</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="71f8f-156">D3D12 n’a plus de fonctionnalité de génération de mipmap dédiée.</span><span class="sxs-lookup"><span data-stu-id="71f8f-156">D3D12 no longer has a dedicated mipmap generation functionality.</span></span> <span data-ttu-id="71f8f-157">Les applications doivent les implémenter de manière autonome à l’aide de nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="71f8f-157">Applications must implement it on their own using shaders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="71f8f-158">D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-158">D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-159">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="71f8f-159">RenderTarget</span></span></td>
<td><span data-ttu-id="71f8f-160">D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-160">D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-161">D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-161">D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-162">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="71f8f-162">Blendable RenderTarget</span></span></td>
<td><span data-ttu-id="71f8f-163">D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-163">D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-164">D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-164">D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-165">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="71f8f-165">Output Merger Logic Op</span></span></td>
<td><span data-ttu-id="71f8f-166">D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</span><span class="sxs-lookup"><span data-stu-id="71f8f-166">D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</span></span></td>
<td><span data-ttu-id="71f8f-167">D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-167">D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-168">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="71f8f-168">Depth/Stencil Target</span></span></td>
<td><span data-ttu-id="71f8f-169">D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-169">D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-170">D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-170">D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-171">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="71f8f-171">Raw UAV and SRV</span></span></td>


</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-172">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="71f8f-172">Structured UAV and SRV</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-173">UAV typé</span><span class="sxs-lookup"><span data-stu-id="71f8f-173">Typed UAV</span></span></td>
<td><span data-ttu-id="71f8f-174">D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-174">D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-175">D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-175">D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-176">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="71f8f-176">UAV Typed Store</span></span></td>
<td><span data-ttu-id="71f8f-177">D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-177">D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-178">D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-178">D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-179">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="71f8f-179">UAV Typed Load</span></span></td>
<td><span data-ttu-id="71f8f-180">D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-180">D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-181">D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-181">D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-182">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="71f8f-182">UAV Atomic Add</span></span></td>
<td><span data-ttu-id="71f8f-183">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-183">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-184">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-184">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-185">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="71f8f-185">UAV Atomic Bitwise Ops</span></span></td>
<td><span data-ttu-id="71f8f-186">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-186">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-187">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-187">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-188">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="71f8f-188">UAV Atomic Cmp&Store/ Cmp&Exch</span></span></td>
<td><span data-ttu-id="71f8f-189">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-189">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-190">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-190">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-191">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="71f8f-191">UAV Atomic Exchange</span></span></td>
<td><span data-ttu-id="71f8f-192">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-192">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-193">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-193">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-194">Min/max signé UAV</span><span class="sxs-lookup"><span data-stu-id="71f8f-194">UAV Atomic Signed Min/Max</span></span></td>
<td><span data-ttu-id="71f8f-195">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-195">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-196">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-196">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-197">UAV Atomic non signé min/max</span><span class="sxs-lookup"><span data-stu-id="71f8f-197">UAV Atomic Unsigned Min/Max</span></span></td>
<td><span data-ttu-id="71f8f-198">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-198">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-199">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-199">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-200">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="71f8f-200">CPU Lockable</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="71f8f-201">Seul un format exclut l’accès au processeur (420_OPAQUE).</span><span class="sxs-lookup"><span data-stu-id="71f8f-201">Only a single format precludes cpu access (420_OPAQUE).</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="71f8f-202">D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-202">D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-203">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="71f8f-203">4x Multisample RenderTarget</span></span></td>
<td><span data-ttu-id="71f8f-204">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-204">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-205">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-205">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-206">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="71f8f-206">8x Multisample RenderTarget</span></span></td>
<td><span data-ttu-id="71f8f-207">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-207">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-208">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-208">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-209">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="71f8f-209">Other Multisample Count RT</span></span></td>
<td><span data-ttu-id="71f8f-210">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-210">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-211">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-211">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-212">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="71f8f-212">Multisample Resolve</span></span></td>
<td><span data-ttu-id="71f8f-213">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-213">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-214">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-214">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-215">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="71f8f-215">Multisample Load</span></span></td>
<td><span data-ttu-id="71f8f-216">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-216">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-217">D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-217">D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-218">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="71f8f-218">Display Scan-Out</span></span></td>
<td><span data-ttu-id="71f8f-219">D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-219">D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-220">D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-220">D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-221">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="71f8f-221">Cast Within Bit Layout</span></span></td>
<td><span data-ttu-id="71f8f-222">D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-222">D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-223">D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-223">D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-224">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="71f8f-224">Video Decoder Support</span></span></td>
<td><span data-ttu-id="71f8f-225">D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-225">D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-226">D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-226">D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-227">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="71f8f-227">Video Processor Input</span></span></td>
<td><span data-ttu-id="71f8f-228">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-228">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-229">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-229">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-230">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="71f8f-230">Video Processor Output</span></span></td>
<td><span data-ttu-id="71f8f-231">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-231">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-232">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-232">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-233">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="71f8f-233">Shared Resource</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="71f8f-234">Les textures de tous les formats peuvent être des ressources validées partagées ou être placées dans des tas partagés.</span><span class="sxs-lookup"><span data-stu-id="71f8f-234">Textures of all formats may be shared committed resources or be placed in shared heaps.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="71f8f-235">D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-235">D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-236">Mémoire tampon en dessous castable même entièrement typée</span><span class="sxs-lookup"><span data-stu-id="71f8f-236">BackBuffer Castable Even Fully Typed</span></span></td>
<td><span data-ttu-id="71f8f-237">D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-237">D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="71f8f-238">Aucune API disponible.</span><span class="sxs-lookup"><span data-stu-id="71f8f-238">No API available.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-239">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="71f8f-239">Tiled Resource</span></span></td>
<td><span data-ttu-id="71f8f-240">D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-240">D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-241">D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-241">D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71f8f-242">Encodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="71f8f-242">Video Encoder</span></span></td>
<td><span data-ttu-id="71f8f-243">D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-243">D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER(<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-244">D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-244">D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71f8f-245">Superposition Multiplan</span><span class="sxs-lookup"><span data-stu-id="71f8f-245">Multiplane Overlay</span></span></td>
<td><span data-ttu-id="71f8f-246">D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-246">D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="71f8f-247">D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="71f8f-247">D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="71f8f-248">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71f8f-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71f8f-249">Niveaux de fonctionnalité matérielle D3D12</span><span class="sxs-lookup"><span data-stu-id="71f8f-249">D3D12 Hardware Feature Levels</span></span>](/windows/desktop/direct3d12/hardware-feature-levels)
</dt> <dt>

[<span data-ttu-id="71f8f-250">**\_format dxgi**</span><span class="sxs-lookup"><span data-stu-id="71f8f-250">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> <dt>

[<span data-ttu-id="71f8f-251">**\_ \_ Prise en charge du format d3d11**</span><span class="sxs-lookup"><span data-stu-id="71f8f-251">**D3D11\_FORMAT\_SUPPORT**</span></span>](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support)
</dt> <dt>

[<span data-ttu-id="71f8f-252">**\_Format d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="71f8f-252">**D3D11\_FORMAT\_SUPPORT2**</span></span>](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2)
</dt> <dt>

[<span data-ttu-id="71f8f-253">Guide de programmation pour DXGI</span><span class="sxs-lookup"><span data-stu-id="71f8f-253">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

