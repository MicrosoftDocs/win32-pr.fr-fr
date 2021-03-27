---
title: Structures de nuanceur (graphiques Direct3D 11)
description: Les structures sont utilisées pour créer et utiliser des nuanceurs.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- structures, nuanceurs Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739589"
---
# <a name="shader-structures-direct3d-11-graphics"></a><span data-ttu-id="4a3c8-104">Structures de nuanceur (graphiques Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="4a3c8-104">Shader Structures (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="4a3c8-105">Les structures sont utilisées pour créer et utiliser des nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-105">Structures are used to create and use shaders.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="4a3c8-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="4a3c8-106">In this section</span></span>



| <span data-ttu-id="4a3c8-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="4a3c8-107">Topic</span></span>                                                                                       | <span data-ttu-id="4a3c8-108">Description</span><span class="sxs-lookup"><span data-stu-id="4a3c8-108">Description</span></span>                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="4a3c8-109">**Description de l’instance de la \_ classe d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-109">**D3D11\_CLASS\_INSTANCE\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | <span data-ttu-id="4a3c8-110">Décrit une instance de classe HLSL.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-110">Describes an HLSL class instance.</span></span><br/>                           |
| [<span data-ttu-id="4a3c8-111">**\_Trace du nuanceur de calcul d3d11 \_ \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-111">**D3D11\_COMPUTE\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | <span data-ttu-id="4a3c8-112">Décrit une instance d’un nuanceur de calcul à tracer.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-112">Describes an instance of a compute shader to trace.</span></span><br/>         |
| [<span data-ttu-id="4a3c8-113">**\_Description de \_ trace du nuanceur de domaine d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-113">**D3D11\_DOMAIN\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | <span data-ttu-id="4a3c8-114">Décrit une instance d’un nuanceur de domaine à tracer.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-114">Describes an instance of a domain shader to trace.</span></span><br/>          |
| [<span data-ttu-id="4a3c8-115">**Description de la \_ fonction d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-115">**D3D11\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | <span data-ttu-id="4a3c8-116">Décrit une fonction.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-116">Describes a function.</span></span><br/>                                       |
| [<span data-ttu-id="4a3c8-117">**Description de la \_ \_ trace du nuanceur GEOMETRy d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-117">**D3D11\_GEOMETRY\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | <span data-ttu-id="4a3c8-118">Décrit une instance d’un nuanceur Geometry à tracer.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-118">Describes an instance of a geometry shader to trace.</span></span><br/>        |
| [<span data-ttu-id="4a3c8-119">**DESC D3D11 de \_ \_ nuanceur de coque \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-119">**D3D11\_HULL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | <span data-ttu-id="4a3c8-120">Décrit une instance d’un nuanceur de coque à tracer.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-120">Describes an instance of a hull shader to trace.</span></span><br/>            |
| [<span data-ttu-id="4a3c8-121">**Description de la \_ bibliothèque d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-121">**D3D11\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | <span data-ttu-id="4a3c8-122">Décrit une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-122">Describes a library.</span></span><br/>                                        |
| [<span data-ttu-id="4a3c8-123">**\_Description du paramètre d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-123">**D3D11\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | <span data-ttu-id="4a3c8-124">Décrit un paramètre de fonction.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-124">Describes a function parameter.</span></span> <br/>                            |
| [<span data-ttu-id="4a3c8-125">**\_Desc de \_ trace de nuanceur de pixels d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-125">**D3D11\_PIXEL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | <span data-ttu-id="4a3c8-126">Décrit une instance d’un nuanceur de pixels à tracer.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-126">Describes an instance of a pixel shader to trace.</span></span><br/>           |
| [<span data-ttu-id="4a3c8-127">**Description de la \_ \_ mémoire tampon du NUANCEur d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-127">**D3D11\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | <span data-ttu-id="4a3c8-128">Décrit une mémoire tampon de nuanceur constante.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-128">Describes a shader constant-buffer.</span></span><br/>                         |
| [<span data-ttu-id="4a3c8-129">**D3D11 \_ Shader \_ desc**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-129">**D3D11\_SHADER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | <span data-ttu-id="4a3c8-130">Décrit un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-130">Describes a shader.</span></span><br/>                                         |
| [<span data-ttu-id="4a3c8-131">**\_Liaison d’entrée de nuanceur d3d11 \_ \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-131">**D3D11\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | <span data-ttu-id="4a3c8-132">Décrit comment une ressource de nuanceur est liée à une entrée de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-132">Describes how a shader resource is bound to a shader input.</span></span><br/> |
| [<span data-ttu-id="4a3c8-133">**\_Trace du nuanceur d3d11 \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-133">**D3D11\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | <span data-ttu-id="4a3c8-134">Décrit un objet Shader-trace.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-134">Describes a shader-trace object.</span></span><br/>                            |
| [<span data-ttu-id="4a3c8-135">**\_Type de nuanceur d3d11 \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-135">**D3D11\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | <span data-ttu-id="4a3c8-136">Décrit un type de variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-136">Describes a shader-variable type.</span></span><br/>                           |
| [<span data-ttu-id="4a3c8-137">**Description de la \_ variable de nuanceur d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-137">**D3D11\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | <span data-ttu-id="4a3c8-138">Décrit une variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-138">Describes a shader variable.</span></span><br/>                                |
| [<span data-ttu-id="4a3c8-139">**\_Description du \_ paramètre de signature d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-139">**D3D11\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | <span data-ttu-id="4a3c8-140">Décrit une signature de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-140">Describes a shader signature.</span></span><br/>                               |
| [<span data-ttu-id="4a3c8-141">**\_Registre de suivi d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-141">**D3D11\_TRACE\_REGISTER**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | <span data-ttu-id="4a3c8-142">Décrit un registre de trace.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-142">Describes a trace register.</span></span><br/>                                 |
| [<span data-ttu-id="4a3c8-143">**\_Statistiques de suivi d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-143">**D3D11\_TRACE\_STATS**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | <span data-ttu-id="4a3c8-144">Spécifie des statistiques sur une trace.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-144">Specifies statistics about a trace.</span></span><br/>                         |
| [<span data-ttu-id="4a3c8-145">**\_Étape de suivi d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-145">**D3D11\_TRACE\_STEP**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | <span data-ttu-id="4a3c8-146">Décrit une étape de trace, qui est une instruction.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-146">Describes a trace step, which is an instruction.</span></span><br/>            |
| [<span data-ttu-id="4a3c8-147">**\_Valeur de trace d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-147">**D3D11\_TRACE\_VALUE**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | <span data-ttu-id="4a3c8-148">Décrit une valeur de trace.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-148">Describes a trace value.</span></span><br/>                                    |
| [<span data-ttu-id="4a3c8-149">**\_Desc d3d11 vertex \_ Shader \_ trace \_**</span><span class="sxs-lookup"><span data-stu-id="4a3c8-149">**D3D11\_VERTEX\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | <span data-ttu-id="4a3c8-150">Décrit une instance d’un nuanceur de sommets à tracer.</span><span class="sxs-lookup"><span data-stu-id="4a3c8-150">Describes an instance of a vertex shader to trace.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="4a3c8-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a3c8-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a3c8-152">Référence du nuanceur</span><span class="sxs-lookup"><span data-stu-id="4a3c8-152">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





