---
title: Structures de nuanceur (Direct3D 12 Graphics)
description: d3d12shader. h déclare les structures suivantes, qui sont utilisées pour créer et utiliser des nuanceurs.
ms.assetid: b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0
keywords:
- structures, nuanceurs Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400d50c48b8b94fc9a59d8e48179aae43e14a4f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106512540"
---
# <a name="shader-structures-direct3d-12-graphics"></a><span data-ttu-id="eb54f-104">Structures de nuanceur (Direct3D 12 Graphics)</span><span class="sxs-lookup"><span data-stu-id="eb54f-104">Shader Structures (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="eb54f-105">d3d12shader. h déclare les structures suivantes, qui sont utilisées pour créer et utiliser des nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="eb54f-105">d3d12shader.h declares the following structures, which are used to create and use shaders.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eb54f-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="eb54f-106">In this section</span></span>



| <span data-ttu-id="eb54f-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="eb54f-107">Topic</span></span>                                                                                  | <span data-ttu-id="eb54f-108">Description</span><span class="sxs-lookup"><span data-stu-id="eb54f-108">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="eb54f-109">**Description de la \_ fonction D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="eb54f-109">**D3D12\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_function_desc)<br/>                        | <span data-ttu-id="eb54f-110">Décrit une fonction.</span><span class="sxs-lookup"><span data-stu-id="eb54f-110">Describes a function.</span></span> <br/>                                       |
| [<span data-ttu-id="eb54f-111">**Description de la \_ bibliothèque D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="eb54f-111">**D3D12\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_library_desc)<br/>                          | <span data-ttu-id="eb54f-112">Décrit une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="eb54f-112">Describes a library.</span></span> <br/>                                        |
| [<span data-ttu-id="eb54f-113">**\_Description du paramètre D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="eb54f-113">**D3D12\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_parameter_desc)<br/>                      | <span data-ttu-id="eb54f-114">Décrit un paramètre de fonction.</span><span class="sxs-lookup"><span data-stu-id="eb54f-114">Describes a function parameter.</span></span> <br/>                             |
| [<span data-ttu-id="eb54f-115">**Description de la \_ \_ mémoire tampon du NUANCEur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="eb54f-115">**D3D12\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_buffer_desc)<br/>             | <span data-ttu-id="eb54f-116">Décrit une mémoire tampon de nuanceur constante.</span><span class="sxs-lookup"><span data-stu-id="eb54f-116">Describes a shader constant-buffer.</span></span> <br/>                         |
| [<span data-ttu-id="eb54f-117">**D3D12 \_ Shader \_ desc**</span><span class="sxs-lookup"><span data-stu-id="eb54f-117">**D3D12\_SHADER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_desc)<br/>                            | <span data-ttu-id="eb54f-118">Décrit un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="eb54f-118">Describes a shader.</span></span> <br/>                                         |
| [<span data-ttu-id="eb54f-119">**\_Liaison d’entrée de nuanceur D3D12 \_ \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="eb54f-119">**D3D12\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc)<br/>    | <span data-ttu-id="eb54f-120">Décrit comment une ressource de nuanceur est liée à une entrée de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="eb54f-120">Describes how a shader resource is bound to a shader input.</span></span> <br/> |
| [<span data-ttu-id="eb54f-121">**\_Type de nuanceur D3D12 \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="eb54f-121">**D3D12\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_type_desc)<br/>                 | <span data-ttu-id="eb54f-122">Décrit un type de variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="eb54f-122">Describes a shader-variable type.</span></span> <br/>                           |
| [<span data-ttu-id="eb54f-123">**Description de la \_ variable de nuanceur D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb54f-123">**D3D12\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_variable_desc)<br/>         | <span data-ttu-id="eb54f-124">Décrit une variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="eb54f-124">Describes a shader variable.</span></span> <br/>                                |
| [<span data-ttu-id="eb54f-125">**\_Description du \_ paramètre de signature D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="eb54f-125">**D3D12\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_signature_parameter_desc)<br/> | <span data-ttu-id="eb54f-126">Décrit une signature de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="eb54f-126">Describes a shader signature.</span></span> <br/>                               |



 

## <a name="related-topics"></a><span data-ttu-id="eb54f-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb54f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb54f-128">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="eb54f-128">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="eb54f-129">Référence du nuanceur</span><span class="sxs-lookup"><span data-stu-id="eb54f-129">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





