---
title: Structure CD3DX12_DEPTH_STENCIL_DESC1 (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une \_ structure DESC1 de stencil de profondeur D3D12 \_ \_ .
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- Structure CD3DX12_DEPTH_STENCIL_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538053"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a><span data-ttu-id="a6454-104">\_ \_ Structure DESC1 du stencil de profondeur CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="a6454-104">CD3DX12\_DEPTH\_STENCIL\_DESC1 structure</span></span>

<span data-ttu-id="a6454-105">Une structure d’assistance pour faciliter l’initialisation d’une structure [**\_ DESC1 de \_ stencil \_ de profondeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .</span><span class="sxs-lookup"><span data-stu-id="a6454-105">A helper structure to enable easy initialization of a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6454-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6454-106">Syntax</span></span>


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="a6454-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a6454-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a6454-108">**CD3DX12 \_ de profondeur du \_ stencil \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="a6454-108">**CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="a6454-109">Crée une nouvelle instance non initialisée d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="a6454-109">Creates a new, uninitialized, instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="a6454-110">**\_stencil de profondeur CD3DX12 explicite \_ \_ DESC1 (const D3D12 de \_ profondeur du \_ stencil \_ DESC1& o)**</span><span class="sxs-lookup"><span data-stu-id="a6454-110">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC1& o)**</span></span>
</dt> <dd>

<span data-ttu-id="a6454-111">Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs copiées à partir d’une structure DESC1 de [**\_ stencil de profondeur \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .</span><span class="sxs-lookup"><span data-stu-id="a6454-111">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a6454-112">**\_stencil de profondeur CD3DX12 explicite \_ \_ DESC1 (const \_ D3D12 \_ desc du stencil \_& o)**</span><span class="sxs-lookup"><span data-stu-id="a6454-112">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(const D3D12\_DEPTH\_STENCIL\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="a6454-113">Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs copiées à partir d’une structure DESC du [**\_ stencil de profondeur \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="a6454-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with values copied from a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) structure</span></span>

<span data-ttu-id="a6454-114">et le membre **DepthBoundsTestEnable** supplémentaire défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="a6454-114">and the additional **DepthBoundsTestEnable** member set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6454-115">**CD3DX12 \_ de profondeur du \_ stencil explicite \_ DESC1 (CD3DX12 \_ par défaut)**</span><span class="sxs-lookup"><span data-stu-id="a6454-115">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="a6454-116">Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec l’État par défaut prescrit par D3DX12 :</span><span class="sxs-lookup"><span data-stu-id="a6454-116">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the default state prescribed by D3DX12:</span></span>

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

<span data-ttu-id="a6454-117">**CD3DX12 de \_ profondeur \_ explicite \_ DESC1 (bool depthEnable, D3D12 \_ masque d’écriture de profondeur \_ \_ depthWriteMask, D3D12 de comparaison DepthFunc, \_ \_ bool STENCILENABLE, UInt8 StencilReadMask, UINT8 stencilWriteMask, D3D12 stencil op frontStencilFailOp, D3D12 stencil op frontStencilDepthFailOp, D3D12 stencil op FRONTSTENCILPASSOP, D3D12 de comparaison Func frontStencilFunc, D3D12 stencil op backStencilFailOp, D3D12 stencil op backStencilDepthFailOp, D3D12 stencil op BACKSTENCILPASSOP, D3D12 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ de comparaison Func backStencilFunc, bool depthBoundsTestEnable)**</span><span class="sxs-lookup"><span data-stu-id="a6454-117">**explicit CD3DX12\_DEPTH\_STENCIL\_DESC1(BOOL depthEnable, D3D12\_DEPTH\_WRITE\_MASK depthWriteMask, D3D12\_COMPARISON\_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12\_STENCIL\_OP frontStencilFailOp, D3D12\_STENCIL\_OP frontStencilDepthFailOp, D3D12\_STENCIL\_OP frontStencilPassOp, D3D12\_COMPARISON\_FUNC frontStencilFunc, D3D12\_STENCIL\_OP backStencilFailOp, D3D12\_STENCIL\_OP backStencilDepthFailOp, D3D12\_STENCIL\_OP backStencilPassOp, D3D12\_COMPARISON\_FUNC backStencilFunc, BOOL depthBoundsTestEnable)**</span></span>
</dt> <dd>

<span data-ttu-id="a6454-118">Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs passées dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="a6454-118">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="a6454-119">**~ CD3DX12 \_ de profondeur du \_ stencil \_ DESC1 ()**</span><span class="sxs-lookup"><span data-stu-id="a6454-119">**~CD3DX12\_DEPTH\_STENCIL\_DESC1()**</span></span>
</dt> <dd>

<span data-ttu-id="a6454-120">Détruit une instance d’un stencil de \_ profondeur \_ D3DX12 \_ DESC1.</span><span class="sxs-lookup"><span data-stu-id="a6454-120">Destroys an instance of a D3DX12\_DEPTH\_STENCIL\_DESC1.</span></span>

</dd> <dt>

<span data-ttu-id="a6454-121">**@ const D3D12 \_ de profondeur du \_ STENCIL \_ DESC1& () const**</span><span class="sxs-lookup"><span data-stu-id="a6454-121">**operator const D3D12\_DEPTH\_STENCIL\_DESC1&() const**</span></span>
</dt> <dd>

<span data-ttu-id="a6454-122">Conversion implicite en \_ structure DESC1 du stencil de profondeur D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a6454-122">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC1 structure.</span></span> <span data-ttu-id="a6454-123">Étant donné \_ que \_ le stencil de profondeur D3D12 \_ DESC1 est le type sous-jacent du \_ stencil de profondeur CD3DX12 \_ \_ DESC1, l’objet est simplement retourné en tant que référence de stencil de profondeur D3D12 const \_ \_ \_ à lui-même.</span><span class="sxs-lookup"><span data-stu-id="a6454-123">Because D3D12\_DEPTH\_STENCIL\_DESC1 is the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> <dt>

<span data-ttu-id="a6454-124">**const D3D12- \_ \_ Description du stencil \_ de profondeur () const**</span><span class="sxs-lookup"><span data-stu-id="a6454-124">**operator const D3D12\_DEPTH\_STENCIL\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="a6454-125">Conversion implicite en \_ valeur de \_ structure DESC du stencil de profondeur D3D12 \_ .</span><span class="sxs-lookup"><span data-stu-id="a6454-125">Implicit conversion to a D3D12\_DEPTH\_STENCIL\_DESC structure value.</span></span> <span data-ttu-id="a6454-126">Étant donné \_ que \_ \_ la description du stencil de profondeur D3D12 n’est pas le type sous-jacent du \_ stencil de profondeur CD3DX12 \_ \_ DESC1, une nouvelle \_ instance DESC du stencil de profondeur D3D12 \_ \_ est créée et retournée par valeur.</span><span class="sxs-lookup"><span data-stu-id="a6454-126">Because D3D12\_DEPTH\_STENCIL\_DESC is not the underlying type of CD3DX12\_DEPTH\_STENCIL\_DESC1, a new D3D12\_DEPTH\_STENCIL\_DESC instance is created and returned by value.</span></span> <span data-ttu-id="a6454-127">Notez que la \_ Description du stencil D3D12 Depth \_ \_ n’inclut pas le membre **DepthBoundsTestEnable** . cette valeur est donc perdue lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="a6454-127">Note that D3D12\_DEPTH\_STENCIL\_DESC does not include the **DepthBoundsTestEnable** member, so this value is lost in the conversion.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6454-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6454-128">Requirements</span></span>



| <span data-ttu-id="a6454-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6454-129">Requirement</span></span> | <span data-ttu-id="a6454-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6454-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a6454-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6454-131">Header</span></span><br/> | <dl> <span data-ttu-id="a6454-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6454-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6454-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6454-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6454-134">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="a6454-134">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a6454-135">**D3D12 \_ du \_ stencil de profondeur \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="a6454-135">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[<span data-ttu-id="a6454-136">**\_Description du \_ stencil de profondeur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="a6454-136">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





