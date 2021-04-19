---
title: Interfaces du nuanceur (Direct3D 12 Graphics)
description: D3d12shader. h déclare les interfaces suivantes.
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- interfaces, nuanceur Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f111572aacca36f12600b0cf334895684064e5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509491"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a><span data-ttu-id="bf5a9-104">Interfaces du nuanceur (Direct3D 12 Graphics)</span><span class="sxs-lookup"><span data-stu-id="bf5a9-104">Shader Interfaces (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="bf5a9-105">d3d12shader. h déclare les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-105">d3d12shader.h declares the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bf5a9-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="bf5a9-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf5a9-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bf5a9-107">Topic</span></span></th>
<th><span data-ttu-id="bf5a9-108">Description</span><span class="sxs-lookup"><span data-stu-id="bf5a9-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf5a9-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf5a9-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="bf5a9-110">Une interface de fonction-paramètre-Reflection accède aux informations sur les paramètres de fonction.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-110">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bf5a9-111">Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 12 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-111">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf5a9-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf5a9-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="bf5a9-113">Une interface de réflexion de fonction accède aux informations de la fonction.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-113">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bf5a9-114">Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 12 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-114">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf5a9-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf5a9-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="bf5a9-116">Une interface de réflexion de bibliothèque accède aux informations de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-116">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bf5a9-117">Cette interface fait partie de la technologie de liaison de nuanceur HLSL que vous pouvez utiliser sur toutes les plateformes Direct3D 12 pour créer des fonctions HLSL précompilées, les empaqueter dans des bibliothèques et les lier à des nuanceurs complets au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-117">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf5a9-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf5a9-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="bf5a9-119">Une interface de nuanceur-réflexion accède à des informations de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-119">A shader-reflection interface accesses shader information.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf5a9-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf5a9-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="bf5a9-121">Cette interface de nuanceur-réflexion fournit l’accès à une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-121">This shader-reflection interface provides access to a constant buffer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf5a9-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf5a9-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="bf5a9-123">Cette interface de nuanceur-réflexion donne accès au type de variable.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-123">This shader-reflection interface provides access to variable type.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf5a9-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf5a9-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="bf5a9-125">Cette interface de nuanceur-réflexion donne accès à une variable.</span><span class="sxs-lookup"><span data-stu-id="bf5a9-125">This shader-reflection interface provides access to a variable.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="bf5a9-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf5a9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf5a9-127">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="bf5a9-127">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="bf5a9-128">Référence du nuanceur</span><span class="sxs-lookup"><span data-stu-id="bf5a9-128">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





