---
title: Structure CD3DX12_DEPTH_STENCIL_DESC (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation facile d’une \_ structure DESC du stencil de profondeur D3D12 \_ \_ .
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- Structure CD3DX12_DEPTH_STENCIL_DESC
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522574"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a><span data-ttu-id="7fa27-104">\_ \_ Structure DESC du stencil de profondeur CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="7fa27-104">CD3DX12\_DEPTH\_STENCIL\_DESC structure</span></span>

<span data-ttu-id="7fa27-105">Une structure d’assistance pour permettre l’initialisation facile d’une [**structure \_ \_ \_ desc du stencil de profondeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="7fa27-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa27-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fa27-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="7fa27-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7fa27-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7fa27-108">**\_Description du \_ stencil de profondeur CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="7fa27-108">**CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="7fa27-109">Crée une nouvelle instance non initialisée d’une \_ Description du stencil de profondeur D3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7fa27-109">Creates a new, uninitialized, instance of a D3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="7fa27-110">**DESC du stencil de profondeur CD3DX12 explicite \_ \_ \_ (const D3D12 \_ profondeur du \_ stencil \_& o)**</span><span class="sxs-lookup"><span data-stu-id="7fa27-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="7fa27-111">Crée une nouvelle instance d’une \_ Description du stencil de profondeur D3DX12 \_ \_ , initialisée avec le contenu d’une autre structure DESC du [**\_ stencil de profondeur \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .</span><span class="sxs-lookup"><span data-stu-id="7fa27-111">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with the contents of another [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7fa27-112">**DESC du \_ stencil de profondeur CD3DX12 explicite \_ \_ (CD3DX12 \_ par défaut)**</span><span class="sxs-lookup"><span data-stu-id="7fa27-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="7fa27-113">Crée une nouvelle instance d’une \_ Description du stencil de profondeur D3DX12 \_ \_ , initialisée avec les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="7fa27-113">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initialized with default parameters.</span></span>

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

<span data-ttu-id="7fa27-114">**Description du \_ \_ stencil de profondeur de CD3DX12 explicite \_ desc (bool depthEnable, D3D12 de \_ profondeur d' \_ écriture \_ depthWriteMask, D3D12 de \_ comparaison depthFunc \_ , bool STENCILENABLE, UInt8 StencilReadMask, UINT8 stencilWriteMask, D3D12 stencil op frontStencilFailOp, D3D12 stencil op frontStencilDepthFailOp, D3D12 stencil op frontStencilPassOp, D3D12 \_ \_ \_ \_ \_ \_ \_ comparaison \_ Func frontStencilFunc, D3D12 \_ stencil op backStencilFailOp, D3D12 stencil op backStencilDepthFailOp, D3D12 \_ \_ \_ \_ stencil op backStencilPassOp, D3D12 \_ \_ comparaison \_ Func backStencilFunc)**</span><span class="sxs-lookup"><span data-stu-id="7fa27-114">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc)**</span></span>
</dt> <dd>

<span data-ttu-id="7fa27-115">Crée une nouvelle instance d’une \_ Description du stencil de profondeur D3DX12 \_ \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7fa27-115">Creates a new instance of a D3DX12\_DEPTH\_STENCIL\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="7fa27-116">BOOL depthEnable</span><span class="sxs-lookup"><span data-stu-id="7fa27-116">BOOL depthEnable</span></span>

<span data-ttu-id="7fa27-117">[**D3D12 \_ \_ \_ Masque d’écriture de profondeur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span><span class="sxs-lookup"><span data-stu-id="7fa27-117">[**D3D12\_DEPTH\_WRITE\_MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask</span></span>

<span data-ttu-id="7fa27-118">[**D3D12 \_ Fonction \_ de comparaison**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc</span><span class="sxs-lookup"><span data-stu-id="7fa27-118">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc</span></span>

<span data-ttu-id="7fa27-119">BOOL stencilEnable</span><span class="sxs-lookup"><span data-stu-id="7fa27-119">BOOL stencilEnable</span></span>

<span data-ttu-id="7fa27-120">UINT8 stencilReadMask</span><span class="sxs-lookup"><span data-stu-id="7fa27-120">UINT8 stencilReadMask</span></span>

<span data-ttu-id="7fa27-121">UINT8 stencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="7fa27-121">UINT8 stencilWriteMask</span></span>

<span data-ttu-id="7fa27-122">[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp</span><span class="sxs-lookup"><span data-stu-id="7fa27-122">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp</span></span>

<span data-ttu-id="7fa27-123">[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp</span><span class="sxs-lookup"><span data-stu-id="7fa27-123">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp</span></span>

<span data-ttu-id="7fa27-124">[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp</span><span class="sxs-lookup"><span data-stu-id="7fa27-124">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp</span></span>

<span data-ttu-id="7fa27-125">[**D3D12 \_ Fonction \_ de comparaison**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc</span><span class="sxs-lookup"><span data-stu-id="7fa27-125">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc</span></span>

<span data-ttu-id="7fa27-126">[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp</span><span class="sxs-lookup"><span data-stu-id="7fa27-126">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp</span></span>

<span data-ttu-id="7fa27-127">[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp</span><span class="sxs-lookup"><span data-stu-id="7fa27-127">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp</span></span>

<span data-ttu-id="7fa27-128">[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp</span><span class="sxs-lookup"><span data-stu-id="7fa27-128">[**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp</span></span>

<span data-ttu-id="7fa27-129">[**D3D12 \_ Fonction \_ de comparaison**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc</span><span class="sxs-lookup"><span data-stu-id="7fa27-129">[**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc</span></span>

</dd> <dt>

<span data-ttu-id="7fa27-130">**~ CD3DX12 \_ du \_ stencil \_ de profondeur ()**</span><span class="sxs-lookup"><span data-stu-id="7fa27-130">**~CD3DX12\_DEPTH\_STENCIL\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="7fa27-131">Détruit une instance d’une description du \_ stencil de profondeur CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7fa27-131">Destroys an instance of a CD3DX12\_DEPTH\_STENCIL\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="7fa27-132">**const D3D12- \_ \_ Description du stencil de profondeur \_& () const**</span><span class="sxs-lookup"><span data-stu-id="7fa27-132">**operator const D3D12\_DEPTH\_STENCIL\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="7fa27-133">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="7fa27-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fa27-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fa27-134">Requirements</span></span>



| <span data-ttu-id="7fa27-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fa27-135">Requirement</span></span> | <span data-ttu-id="7fa27-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fa27-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa27-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fa27-137">Header</span></span><br/> | <dl> <span data-ttu-id="7fa27-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fa27-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fa27-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fa27-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa27-140">**\_Description du \_ stencil de profondeur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7fa27-140">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[<span data-ttu-id="7fa27-141">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="7fa27-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





