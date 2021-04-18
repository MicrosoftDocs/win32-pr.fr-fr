---
title: Structure CD3DX12_BLEND_DESC (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation simple d’une \_ structure D3D12 Blend \_ desc.
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- Structure CD3DX12_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522575"
---
# <a name="cd3dx12_blend_desc-structure"></a><span data-ttu-id="09748-104">CD3DX12 \_ Blend, \_ structure DESC</span><span class="sxs-lookup"><span data-stu-id="09748-104">CD3DX12\_BLEND\_DESC structure</span></span>

<span data-ttu-id="09748-105">Une structure d’assistance pour permettre l’initialisation simple d’une structure [**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .</span><span class="sxs-lookup"><span data-stu-id="09748-105">A helper structure to enable easy initialization of a [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="09748-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09748-106">Syntax</span></span>


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="09748-107">Membres</span><span class="sxs-lookup"><span data-stu-id="09748-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="09748-108">**CD3DX12 \_ Blend \_ desc ()**</span><span class="sxs-lookup"><span data-stu-id="09748-108">**CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="09748-109">Crée une nouvelle instance non initialisée d’un CD3DX12 \_ Blend \_ desc.</span><span class="sxs-lookup"><span data-stu-id="09748-109">Creates a new, uninitialized, instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="09748-110">**explicite CD3DX12 \_ Blend \_ desc (const D3D12 \_ Blend \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="09748-110">**explicit CD3DX12\_BLEND\_DESC(const D3D12\_BLEND\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="09748-111">Crée une nouvelle instance d’un CD3DX12 \_ Blend \_ desc, initialisée avec le contenu d’une autre structure [**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .</span><span class="sxs-lookup"><span data-stu-id="09748-111">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with the contents of another [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="09748-112">**Explicit CD3DX12 \_ Blend \_ desc (CD3DX12 \_ par défaut)**</span><span class="sxs-lookup"><span data-stu-id="09748-112">**explicit CD3DX12\_BLEND\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="09748-113">Crée une nouvelle instance d’un CD3DX12 \_ Blend \_ desc, initialisé avec les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="09748-113">Creates a new instance of a CD3DX12\_BLEND\_DESC, initialized with default parameters.</span></span>



| <span data-ttu-id="09748-114">State</span><span class="sxs-lookup"><span data-stu-id="09748-114">State</span></span>                                   | <span data-ttu-id="09748-115">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="09748-115">Default Value</span></span>                    |
|-----------------------------------------|----------------------------------|
| <span data-ttu-id="09748-116">AlphaToCoverageEnable</span><span class="sxs-lookup"><span data-stu-id="09748-116">AlphaToCoverageEnable</span></span>                   | <span data-ttu-id="09748-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="09748-117">**FALSE**</span></span>                        |
| <span data-ttu-id="09748-118">IndependentBlendEnable</span><span class="sxs-lookup"><span data-stu-id="09748-118">IndependentBlendEnable</span></span>                  | <span data-ttu-id="09748-119">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="09748-119">**FALSE**</span></span>                        |
| <span data-ttu-id="09748-120">RenderTarget \[ 0 \] . BlendEnable</span><span class="sxs-lookup"><span data-stu-id="09748-120">RenderTarget\[0\].BlendEnable</span></span>           | <span data-ttu-id="09748-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="09748-121">**FALSE**</span></span>                        |
| <span data-ttu-id="09748-122">RenderTarget \[ 0 \] . LogicOpEnable</span><span class="sxs-lookup"><span data-stu-id="09748-122">RenderTarget\[0\].LogicOpEnable</span></span>         | <span data-ttu-id="09748-123">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="09748-123">**FALSE**</span></span>                        |
| <span data-ttu-id="09748-124">RenderTarget \[ 0 \] . SrcBlend</span><span class="sxs-lookup"><span data-stu-id="09748-124">RenderTarget\[0\].SrcBlend</span></span>              | <span data-ttu-id="09748-125">D3D12 \_ Blend \_ One</span><span class="sxs-lookup"><span data-stu-id="09748-125">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="09748-126">RenderTarget \[ 0 \] . DestBlend</span><span class="sxs-lookup"><span data-stu-id="09748-126">RenderTarget\[0\].DestBlend</span></span>             | <span data-ttu-id="09748-127">D3D12 \_ Blend \_ zéro</span><span class="sxs-lookup"><span data-stu-id="09748-127">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="09748-128">RenderTarget \[ 0 \] . BlendOp</span><span class="sxs-lookup"><span data-stu-id="09748-128">RenderTarget\[0\].BlendOp</span></span>               | <span data-ttu-id="09748-129">\_Ajouter D3D12 Blend \_ op \_</span><span class="sxs-lookup"><span data-stu-id="09748-129">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="09748-130">RenderTarget \[ 0 \] . SrcBlendAlpha</span><span class="sxs-lookup"><span data-stu-id="09748-130">RenderTarget\[0\].SrcBlendAlpha</span></span>         | <span data-ttu-id="09748-131">D3D12 \_ Blend \_ One</span><span class="sxs-lookup"><span data-stu-id="09748-131">D3D12\_BLEND\_ONE</span></span>                |
| <span data-ttu-id="09748-132">RenderTarget \[ 0 \] . DestBlendAlpha</span><span class="sxs-lookup"><span data-stu-id="09748-132">RenderTarget\[0\].DestBlendAlpha</span></span>        | <span data-ttu-id="09748-133">D3D12 \_ Blend \_ zéro</span><span class="sxs-lookup"><span data-stu-id="09748-133">D3D12\_BLEND\_ZERO</span></span>               |
| <span data-ttu-id="09748-134">RenderTarget \[ 0 \] . BlendOpAlpha</span><span class="sxs-lookup"><span data-stu-id="09748-134">RenderTarget\[0\].BlendOpAlpha</span></span>          | <span data-ttu-id="09748-135">\_Ajouter D3D12 Blend \_ op \_</span><span class="sxs-lookup"><span data-stu-id="09748-135">D3D12\_BLEND\_OP\_ADD</span></span>            |
| <span data-ttu-id="09748-136">RenderTarget \[ 0 \] . LogicOp</span><span class="sxs-lookup"><span data-stu-id="09748-136">RenderTarget\[0\].LogicOp</span></span>               | <span data-ttu-id="09748-137">D3D12 \_ logique \_ op \_</span><span class="sxs-lookup"><span data-stu-id="09748-137">D3D12\_LOGIC\_OP\_NOOP</span></span>           |
| <span data-ttu-id="09748-138">RenderTarget \[ 0 \] . RenderTargetWriteMask</span><span class="sxs-lookup"><span data-stu-id="09748-138">RenderTarget\[0\].RenderTargetWriteMask</span></span> | <span data-ttu-id="09748-139">\_Activer l’écriture en couleur D3D12 \_ \_ \_ tout</span><span class="sxs-lookup"><span data-stu-id="09748-139">D3D12\_COLOR\_WRITE\_ENABLE\_ALL</span></span> |



 

</dd> <dt>

<span data-ttu-id="09748-140">**~ CD3DX12 \_ Blend \_ desc ()**</span><span class="sxs-lookup"><span data-stu-id="09748-140">**~CD3DX12\_BLEND\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="09748-141">Détruit une instance d’un CD3DX12 \_ Blend \_ desc.</span><span class="sxs-lookup"><span data-stu-id="09748-141">Destroys an instance of a CD3DX12\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="09748-142">**const, opérateur D3D12 \_ Blend \_ desc& () const**</span><span class="sxs-lookup"><span data-stu-id="09748-142">**operator const D3D12\_BLEND\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="09748-143">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="09748-143">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09748-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09748-144">Requirements</span></span>



| <span data-ttu-id="09748-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09748-145">Requirement</span></span> | <span data-ttu-id="09748-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="09748-146">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="09748-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="09748-147">Header</span></span><br/> | <dl> <span data-ttu-id="09748-148"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="09748-148"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09748-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09748-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09748-150">**D3D12 \_ Blend \_ desc**</span><span class="sxs-lookup"><span data-stu-id="09748-150">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[<span data-ttu-id="09748-151">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="09748-151">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





