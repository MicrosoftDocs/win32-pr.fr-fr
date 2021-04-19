---
title: Structure CD3DX12_ROOT_PARAMETER1 (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation facile d’une \_ structure de \_ PARAMÈTRE1 racine D3D12.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- Structure CD3DX12_ROOT_PARAMETER1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539921"
---
# <a name="cd3dx12_root_parameter1-structure"></a><span data-ttu-id="7b43e-104">CD3DX12 \_ - \_ structure de paramètre1 racine</span><span class="sxs-lookup"><span data-stu-id="7b43e-104">CD3DX12\_ROOT\_PARAMETER1 structure</span></span>

<span data-ttu-id="7b43e-105">Une structure d’assistance pour permettre l’initialisation facile d’une structure de [**\_ \_ paramètre1 racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .</span><span class="sxs-lookup"><span data-stu-id="7b43e-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b43e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b43e-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="7b43e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7b43e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b43e-108">**CD3DX12 \_ racine \_ paramètre1 ()**</span><span class="sxs-lookup"><span data-stu-id="7b43e-108">**CD3DX12\_ROOT\_PARAMETER1()**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-109">Crée une nouvelle instance non initialisée d’un \_ paramètre1 racine CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="7b43e-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER1.</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-110">**CD3DX12 \_ racine explicite \_ paramètre1 (const D3D12 \_ racine \_ paramètre1 &o)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-110">**explicit CD3DX12\_ROOT\_PARAMETER1(const D3D12\_ROOT\_PARAMETER1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-111">Crée une nouvelle instance d’un \_ paramètre1 racine CD3DX12 \_ , initialisée avec le contenu d’une autre structure [**\_ \_ paramètre1 racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .</span><span class="sxs-lookup"><span data-stu-id="7b43e-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER1, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-112">**static Inline InitAsDescriptorTable (D3D12 \_ racine \_ paramètre1 &ROOTPARAM, uint numDescriptorRanges, CONSt D3D12 \_ descripteur \_ RANGE1 \* pDescriptorRanges, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-113">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b43e-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b43e-114">[**D3D12 \_ &de \_ PARAMÈTRE1 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) rootParam</span><span class="sxs-lookup"><span data-stu-id="7b43e-114">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="7b43e-115">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="7b43e-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="7b43e-116">const [**D3D12 \_ descripteur \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="7b43e-116">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="7b43e-117">[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7b43e-117">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-118">**static Inline InitAsConstants (D3D12 \_ racine \_ paramètre1 &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-119">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b43e-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b43e-120">[**D3D12 \_ &de \_ PARAMÈTRE1 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) rootParam</span><span class="sxs-lookup"><span data-stu-id="7b43e-120">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="7b43e-121">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="7b43e-121">UINT num32BitValues</span></span>

<span data-ttu-id="7b43e-122">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b43e-122">UINT shaderRegister</span></span>

<span data-ttu-id="7b43e-123">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b43e-123">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b43e-124">[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7b43e-124">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-125">**static Inline InitAsConstantBufferView (D3D12 \_ racine \_ paramètre1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ \_ descripteurs racine Flags \_ = D3D12 \_ indicateur de \_ descripteur racine \_ \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-126">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b43e-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b43e-127">[**D3D12 \_ &de \_ PARAMÈTRE1 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) rootParam</span><span class="sxs-lookup"><span data-stu-id="7b43e-127">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="7b43e-128">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b43e-128">UINT shaderRegister</span></span>

<span data-ttu-id="7b43e-129">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b43e-129">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b43e-130">[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="7b43e-130">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="7b43e-131">[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7b43e-131">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-132">**static Inline InitAsShaderResourceView (D3D12 \_ racine \_ paramètre1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ \_ descripteurs racine Flags \_ = D3D12 \_ indicateur de \_ descripteur racine \_ \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-132">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-133">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b43e-133">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b43e-134">[**D3D12 \_ &de \_ PARAMÈTRE1 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) rootParam</span><span class="sxs-lookup"><span data-stu-id="7b43e-134">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="7b43e-135">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b43e-135">UINT shaderRegister</span></span>

<span data-ttu-id="7b43e-136">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b43e-136">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b43e-137">[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="7b43e-137">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="7b43e-138">[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7b43e-138">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-139">**static Inline InitAsUnorderedAccessView (D3D12 \_ racine \_ paramètre1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ \_ descripteurs racine Flags \_ = D3D12 \_ indicateur de \_ descripteur racine \_ \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-139">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-140">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b43e-140">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b43e-141">[**D3D12 \_ &de \_ PARAMÈTRE1 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) rootParam</span><span class="sxs-lookup"><span data-stu-id="7b43e-141">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="7b43e-142">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b43e-142">UINT shaderRegister</span></span>

<span data-ttu-id="7b43e-143">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b43e-143">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b43e-144">[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="7b43e-144">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="7b43e-145">[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7b43e-145">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-146">**Inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ descripteur \_ RANGE1 \* pDescriptorRanges, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-146">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-147">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b43e-147">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b43e-148">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="7b43e-148">UINT numDescriptorRanges</span></span>

<span data-ttu-id="7b43e-149">const [**D3D12 \_ descripteur \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="7b43e-149">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="7b43e-150">[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7b43e-150">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-151">**Inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-151">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-152">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b43e-152">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b43e-153">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="7b43e-153">UINT num32BitValues</span></span>

<span data-ttu-id="7b43e-154">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b43e-154">UINT shaderRegister</span></span>

<span data-ttu-id="7b43e-155">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b43e-155">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b43e-156">[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7b43e-156">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-157">**Inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ \_ descripteur racine Flags \_ = D3D12 \_ \_ indicateur de descripteur racine \_ \_ None, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-157">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-158">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b43e-158">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b43e-159">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b43e-159">UINT shaderRegister</span></span>

<span data-ttu-id="7b43e-160">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b43e-160">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b43e-161">[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="7b43e-161">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="7b43e-162">[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7b43e-162">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-163">**Inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ \_ descripteur racine Flags \_ = D3D12 \_ \_ indicateur de descripteur racine \_ \_ None, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-163">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-164">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b43e-164">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b43e-165">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b43e-165">UINT shaderRegister</span></span>

<span data-ttu-id="7b43e-166">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b43e-166">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b43e-167">[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="7b43e-167">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="7b43e-168">[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7b43e-168">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="7b43e-169">**Inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ \_ descripteur racine Flags \_ = D3D12 \_ \_ indicateur de descripteur racine \_ \_ None, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="7b43e-169">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="7b43e-170">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b43e-170">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b43e-171">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b43e-171">UINT shaderRegister</span></span>

<span data-ttu-id="7b43e-172">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b43e-172">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b43e-173">[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="7b43e-173">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="7b43e-174">[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="7b43e-174">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b43e-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b43e-175">Requirements</span></span>



| <span data-ttu-id="7b43e-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b43e-176">Requirement</span></span> | <span data-ttu-id="7b43e-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b43e-177">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7b43e-178">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b43e-178">Header</span></span><br/> | <dl> <span data-ttu-id="7b43e-179"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b43e-179"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b43e-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b43e-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b43e-181">**D3D12 \_ racine \_ paramètre1**</span><span class="sxs-lookup"><span data-stu-id="7b43e-181">**D3D12\_ROOT\_PARAMETER1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[<span data-ttu-id="7b43e-182">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="7b43e-182">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





