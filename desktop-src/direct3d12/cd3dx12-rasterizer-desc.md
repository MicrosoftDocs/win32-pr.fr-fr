---
title: Structure CD3DX12_RASTERIZER_DESC (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure D3D12 \_ rastériseur \_ desc.
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- Structure CD3DX12_RASTERIZER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535792"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a><span data-ttu-id="05cbd-104">\_Structure CD3DX12 rastériseur \_ desc</span><span class="sxs-lookup"><span data-stu-id="05cbd-104">CD3DX12\_RASTERIZER\_DESC structure</span></span>

<span data-ttu-id="05cbd-105">Structure d’assistance pour permettre l’initialisation facile d’une structure [**D3D12 \_ rastériseur \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .</span><span class="sxs-lookup"><span data-stu-id="05cbd-105">A helper structure to enable easy initialization of a [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="05cbd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05cbd-106">Syntax</span></span>


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="05cbd-107">Membres</span><span class="sxs-lookup"><span data-stu-id="05cbd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="05cbd-108">**CD3DX12 \_ rastériseur \_ desc ()**</span><span class="sxs-lookup"><span data-stu-id="05cbd-108">**CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="05cbd-109">Crée une nouvelle instance non initialisée d’un CD3DX12 \_ rastériseur \_ desc.</span><span class="sxs-lookup"><span data-stu-id="05cbd-109">Creates a new, uninitialized, instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="05cbd-110">**CD3DX12 \_ de rastérisation explicite \_ desc (const D3D12 \_ rastériseur \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="05cbd-110">**explicit CD3DX12\_RASTERIZER\_DESC(const D3D12\_RASTERIZER\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="05cbd-111">Crée une nouvelle instance d’un CD3DX12 \_ rastériseur \_ desc, initialisée avec le contenu d’une autre structure [**D3D12 \_ rastériseur \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .</span><span class="sxs-lookup"><span data-stu-id="05cbd-111">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with the contents of another [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="05cbd-112">**CD3DX12 \_ rastériseur DESC explicite \_ (CD3DX12 \_ par défaut)**</span><span class="sxs-lookup"><span data-stu-id="05cbd-112">**explicit CD3DX12\_RASTERIZER\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="05cbd-113">Crée une nouvelle instance d’un CD3DX12 \_ rastériseur \_ desc, initialisé avec les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="05cbd-113">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initialized with default parameters.</span></span>

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

<span data-ttu-id="05cbd-114">**CD3DX12 \_ rastériseur DESC explicite \_ (D3D12 \_ mode de remplissage \_ fillMode, D3D12 \_ mode d’élimination \_ CullMode, bool FrontCounterClockwise, int DepthBias, float DepthBiasClamp, float SlopeScaledDepthBias, BOOL DepthClipEnable, bool MultisampleEnable, bool antialiasedLineEnable, uint forcedSampleCount, D3D12 \_ mode de pixellisation conservatrice \_ \_ conservativeRaster)**</span><span class="sxs-lookup"><span data-stu-id="05cbd-114">**explicit CD3DX12\_RASTERIZER\_DESC(D3D12\_FILL\_MODE fillMode, D3D12\_CULL\_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE conservativeRaster)**</span></span>
</dt> <dd>

<span data-ttu-id="05cbd-115">Crée une nouvelle instance d’un CD3DX12 \_ rastériseur \_ desc, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="05cbd-115">Creates a new instance of a CD3DX12\_RASTERIZER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="05cbd-116">[**D3D12 \_ \_Mode de remplissage**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span><span class="sxs-lookup"><span data-stu-id="05cbd-116">[**D3D12\_FILL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode</span></span>

<span data-ttu-id="05cbd-117">[**D3D12 \_ \_Mode d’élimination**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode</span><span class="sxs-lookup"><span data-stu-id="05cbd-117">[**D3D12\_CULL\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode</span></span>

<span data-ttu-id="05cbd-118">BOOL frontCounterClockwise</span><span class="sxs-lookup"><span data-stu-id="05cbd-118">BOOL frontCounterClockwise</span></span>

<span data-ttu-id="05cbd-119">INT depthBias</span><span class="sxs-lookup"><span data-stu-id="05cbd-119">INT depthBias</span></span>

<span data-ttu-id="05cbd-120">DepthBiasClamp FLOAT</span><span class="sxs-lookup"><span data-stu-id="05cbd-120">FLOAT depthBiasClamp</span></span>

<span data-ttu-id="05cbd-121">SlopeScaledDepthBias FLOAT</span><span class="sxs-lookup"><span data-stu-id="05cbd-121">FLOAT slopeScaledDepthBias</span></span>

<span data-ttu-id="05cbd-122">BOOL depthClipEnable</span><span class="sxs-lookup"><span data-stu-id="05cbd-122">BOOL depthClipEnable</span></span>

<span data-ttu-id="05cbd-123">BOOL multisampleEnable</span><span class="sxs-lookup"><span data-stu-id="05cbd-123">BOOL multisampleEnable</span></span>

<span data-ttu-id="05cbd-124">BOOL antialiasedLineEnable</span><span class="sxs-lookup"><span data-stu-id="05cbd-124">BOOL antialiasedLineEnable</span></span>

<span data-ttu-id="05cbd-125">UINT forcedSampleCount</span><span class="sxs-lookup"><span data-stu-id="05cbd-125">UINT forcedSampleCount</span></span>

<span data-ttu-id="05cbd-126">[**D3D12 \_ \_ \_ Mode de pixellisation conservateur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span><span class="sxs-lookup"><span data-stu-id="05cbd-126">[**D3D12\_CONSERVATIVE\_RASTERIZATION\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster</span></span>

</dd> <dt>

<span data-ttu-id="05cbd-127">**~ CD3DX12 \_ rastériseur \_ desc ()**</span><span class="sxs-lookup"><span data-stu-id="05cbd-127">**~CD3DX12\_RASTERIZER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="05cbd-128">Détruit une instance d’un CD3DX12 \_ rastériseur \_ desc.</span><span class="sxs-lookup"><span data-stu-id="05cbd-128">Destroys an instance of a CD3DX12\_RASTERIZER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="05cbd-129">**const D3D12, opérateur const \_ \_ descr DESC& () const**</span><span class="sxs-lookup"><span data-stu-id="05cbd-129">**operator const D3D12\_RASTERIZER\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="05cbd-130">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="05cbd-130">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05cbd-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05cbd-131">Requirements</span></span>



| <span data-ttu-id="05cbd-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05cbd-132">Requirement</span></span> | <span data-ttu-id="05cbd-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="05cbd-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="05cbd-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="05cbd-134">Header</span></span><br/> | <dl> <span data-ttu-id="05cbd-135"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="05cbd-135"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05cbd-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05cbd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05cbd-137">**D3D12 \_ rastériseur \_ desc**</span><span class="sxs-lookup"><span data-stu-id="05cbd-137">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[<span data-ttu-id="05cbd-138">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="05cbd-138">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





