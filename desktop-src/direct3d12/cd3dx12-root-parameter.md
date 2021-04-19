---
title: Structure CD3DX12_ROOT_PARAMETER (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de paramètres racine D3D12 \_ .
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- Structure CD3DX12_ROOT_PARAMETER
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529594"
---
# <a name="cd3dx12_root_parameter-structure"></a><span data-ttu-id="f94cf-104">\_Structure de \_ paramètre racine CD3DX12</span><span class="sxs-lookup"><span data-stu-id="f94cf-104">CD3DX12\_ROOT\_PARAMETER structure</span></span>

<span data-ttu-id="f94cf-105">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ paramètres racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .</span><span class="sxs-lookup"><span data-stu-id="f94cf-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f94cf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f94cf-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="f94cf-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f94cf-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f94cf-108">**\_Paramètre racine CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="f94cf-108">**CD3DX12\_ROOT\_PARAMETER()**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-109">Crée une nouvelle instance non initialisée d’un \_ paramètre racine CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="f94cf-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-110">**paramètre racine CD3DX12 explicite \_ \_ (paramètre racine const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-110">**explicit CD3DX12\_ROOT\_PARAMETER(const D3D12\_ROOT\_PARAMETER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-111">Crée une nouvelle instance d’un \_ paramètre racine CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ paramètres racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .</span><span class="sxs-lookup"><span data-stu-id="f94cf-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-112">**static Inline InitAsDescriptorTable (D3D12 \_ \_ paramètre racine &ROOTPARAM, uint numDescriptorRanges, CONSt D3D12 \_ descripteur \_ Range \* pDescriptorRanges, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-113">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f94cf-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f94cf-114">[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="f94cf-114">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="f94cf-115">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="f94cf-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="f94cf-116">[**D3D12 \_ \_Plage de DEscripteurs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="f94cf-116">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="f94cf-117">possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="f94cf-117">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-118">**static Inline InitAsConstants (D3D12 \_ \_ paramètre racine &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-119">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f94cf-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f94cf-120">[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="f94cf-120">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="f94cf-121">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="f94cf-121">UINT num32BitValues</span></span>

<span data-ttu-id="f94cf-122">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f94cf-122">UINT shaderRegister</span></span>

<span data-ttu-id="f94cf-123">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f94cf-123">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="f94cf-124">possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="f94cf-124">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-125">**static Inline InitAsConstantBufferView (D3D12 \_ \_ paramètre racine &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-126">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f94cf-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f94cf-127">[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="f94cf-127">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="f94cf-128">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f94cf-128">UINT shaderRegister</span></span>

<span data-ttu-id="f94cf-129">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f94cf-129">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="f94cf-130">possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="f94cf-130">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-131">**static Inline InitAsShaderResourceView (D3D12 \_ \_ paramètre racine &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-131">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-132">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f94cf-132">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f94cf-133">[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="f94cf-133">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="f94cf-134">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f94cf-134">UINT shaderRegister</span></span>

<span data-ttu-id="f94cf-135">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f94cf-135">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="f94cf-136">possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="f94cf-136">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-137">**static Inline InitAsUnorderedAccessView (D3D12 \_ \_ paramètre racine &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-137">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-138">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f94cf-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f94cf-139">[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="f94cf-139">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="f94cf-140">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f94cf-140">UINT shaderRegister</span></span>

<span data-ttu-id="f94cf-141">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f94cf-141">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="f94cf-142">possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="f94cf-142">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-143">**Inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ descripteur \_ Range \* pDescriptorRanges, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-143">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-144">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f94cf-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f94cf-145">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="f94cf-145">UINT numDescriptorRanges</span></span>

<span data-ttu-id="f94cf-146">[**D3D12 \_ \_Plage de DEscripteurs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="f94cf-146">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="f94cf-147">possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="f94cf-147">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-148">**Inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-148">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-149">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f94cf-149">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f94cf-150">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="f94cf-150">UINT num32BitValues</span></span>

<span data-ttu-id="f94cf-151">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f94cf-151">UINT shaderRegister</span></span>

<span data-ttu-id="f94cf-152">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f94cf-152">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="f94cf-153">possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="f94cf-153">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-154">**Inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-154">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-155">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f94cf-155">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f94cf-156">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f94cf-156">UINT shaderRegister</span></span>

<span data-ttu-id="f94cf-157">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f94cf-157">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="f94cf-158">possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="f94cf-158">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-159">**Inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-159">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-160">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f94cf-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f94cf-161">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f94cf-161">UINT shaderRegister</span></span>

<span data-ttu-id="f94cf-162">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f94cf-162">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="f94cf-163">possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="f94cf-163">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="f94cf-164">**Inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="f94cf-164">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="f94cf-165">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="f94cf-165">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="f94cf-166">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="f94cf-166">UINT shaderRegister</span></span>

<span data-ttu-id="f94cf-167">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="f94cf-167">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="f94cf-168">possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="f94cf-168">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f94cf-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f94cf-169">Requirements</span></span>



| <span data-ttu-id="f94cf-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f94cf-170">Requirement</span></span> | <span data-ttu-id="f94cf-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="f94cf-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f94cf-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="f94cf-172">Header</span></span><br/> | <dl> <span data-ttu-id="f94cf-173"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f94cf-173"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f94cf-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f94cf-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94cf-175">**\_Paramètre racine \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="f94cf-175">**D3D12\_ROOT\_PARAMETER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[<span data-ttu-id="f94cf-176">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="f94cf-176">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





