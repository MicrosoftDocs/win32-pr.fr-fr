---
title: Structure CD3DX12_ROOT_DESCRIPTOR1 (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation facile d’une \_ \_ structure DESCRIPTOR1 racine D3D12.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- Structure CD3DX12_ROOT_DESCRIPTOR1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532482"
---
# <a name="cd3dx12_root_descriptor1-structure"></a><span data-ttu-id="6467a-104">CD3DX12 \_ racine \_ DESCRIPTOR1, structure</span><span class="sxs-lookup"><span data-stu-id="6467a-104">CD3DX12\_ROOT\_DESCRIPTOR1 structure</span></span>

<span data-ttu-id="6467a-105">Une structure d’assistance pour permettre l’initialisation facile d’une [**structure \_ \_ DESCRIPTOR1 racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .</span><span class="sxs-lookup"><span data-stu-id="6467a-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6467a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6467a-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="6467a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6467a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6467a-108">**CD3DX12 \_ racine \_ DESCRIPTOR1 ()**</span><span class="sxs-lookup"><span data-stu-id="6467a-108">**CD3DX12\_ROOT\_DESCRIPTOR1()**</span></span>
</dt> <dd>

<span data-ttu-id="6467a-109">Crée une nouvelle instance non initialisée d’un \_ DESCRIPTOR1 racine CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="6467a-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR1.</span></span>

</dd> <dt>

<span data-ttu-id="6467a-110">**CD3DX12 \_ racine \_ DESCRIPTOR1 explicite (const D3D12 \_ racine \_ DESCRIPTOR1 &o)**</span><span class="sxs-lookup"><span data-stu-id="6467a-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR1(const D3D12\_ROOT\_DESCRIPTOR1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="6467a-111">Crée une nouvelle instance d’un \_ DESCRIPTOR1 racine CD3DX12 \_ , initialisée avec le contenu d’une autre structure [**\_ \_ DESCRIPTOR1 racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .</span><span class="sxs-lookup"><span data-stu-id="6467a-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6467a-112">**CD3DX12 \_ root \_ DESCRIPTOR1 (uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ \_ descripteur racine Flags \_ = D3D12, \_ indicateur de \_ descripteur racine \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="6467a-112">**CD3DX12\_ROOT\_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="6467a-113">Crée une nouvelle instance d’un \_ DESCRIPTOR1 racine CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6467a-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initializing the following parameters:</span></span>

<span data-ttu-id="6467a-114">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6467a-114">UINT shaderRegister</span></span>

<span data-ttu-id="6467a-115">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6467a-115">UINT registerSpace = 0</span></span>

<span data-ttu-id="6467a-116">[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="6467a-116">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="6467a-117">**Inline init (UINT shaderRegister, UINT registerSpace = 0, D3D12 la \_ racine du \_ descripteur Flags \_ = D3D12 \_ \_ , indicateur de descripteur racine \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="6467a-117">**inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="6467a-118">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6467a-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6467a-119">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6467a-119">UINT shaderRegister</span></span>

<span data-ttu-id="6467a-120">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6467a-120">UINT registerSpace = 0</span></span>

<span data-ttu-id="6467a-121">[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="6467a-121">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="6467a-122">**static Inline init (D3D12 \_ racine \_ DESCRIPTOR1 &table, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ \_ descripteurs racine \_ indicateurs Flags = D3D12 \_ \_ indicateur de descripteur racine \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="6467a-122">**static inline Init(D3D12\_ROOT\_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="6467a-123">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6467a-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="6467a-124">[**D3D12 \_ Table &racine \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)</span><span class="sxs-lookup"><span data-stu-id="6467a-124">[**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &table</span></span>

<span data-ttu-id="6467a-125">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="6467a-125">UINT shaderRegister</span></span>

<span data-ttu-id="6467a-126">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="6467a-126">UINT registerSpace = 0</span></span>

<span data-ttu-id="6467a-127">[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="6467a-127">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6467a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6467a-128">Requirements</span></span>



| <span data-ttu-id="6467a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6467a-129">Requirement</span></span> | <span data-ttu-id="6467a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6467a-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6467a-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="6467a-131">Header</span></span><br/> | <dl> <span data-ttu-id="6467a-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6467a-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6467a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6467a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6467a-134">**D3D12 \_ racine \_ DESCRIPTOR1**</span><span class="sxs-lookup"><span data-stu-id="6467a-134">**D3D12\_ROOT\_DESCRIPTOR1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[<span data-ttu-id="6467a-135">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="6467a-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





