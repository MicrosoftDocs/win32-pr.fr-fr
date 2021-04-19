---
title: Structure CD3DX12_TILE_SHAPE (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure de \_ forme de vignette D3D12 \_ .
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- Structure CD3DX12_TILE_SHAPE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531315"
---
# <a name="cd3dx12_tile_shape-structure"></a><span data-ttu-id="aa9df-104">Structure de la \_ forme de vignette CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="aa9df-104">CD3DX12\_TILE\_SHAPE structure</span></span>

<span data-ttu-id="aa9df-105">Structure d’assistance pour permettre l’initialisation facile d’une structure [**de \_ \_ forme de vignette D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .</span><span class="sxs-lookup"><span data-stu-id="aa9df-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9df-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa9df-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a><span data-ttu-id="aa9df-107">Membres</span><span class="sxs-lookup"><span data-stu-id="aa9df-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa9df-108">**\_ \_ Forme de vignette CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="aa9df-108">**CD3DX12\_TILE\_SHAPE()**</span></span>
</dt> <dd>

<span data-ttu-id="aa9df-109">Crée une nouvelle instance non initialisée d’une \_ forme de vignette CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="aa9df-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_SHAPE.</span></span>

</dd> <dt>

<span data-ttu-id="aa9df-110">**\_forme de vignette CD3DX12 explicite \_ (forme de vignette const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="aa9df-110">**explicit CD3DX12\_TILE\_SHAPE(const D3D12\_TILE\_SHAPE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="aa9df-111">Crée une nouvelle instance d’une \_ forme de vignette CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ forme de vignette D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .</span><span class="sxs-lookup"><span data-stu-id="aa9df-111">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initialized with the contents of another [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aa9df-112">**\_ \_ Forme de vignette CD3DX12 (uint WIDTHINTEXELS, uint HEIGHTINTEXELS, uint depthInTexels)**</span><span class="sxs-lookup"><span data-stu-id="aa9df-112">**CD3DX12\_TILE\_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels)**</span></span>
</dt> <dd>

<span data-ttu-id="aa9df-113">Crée une nouvelle instance d’une \_ forme de vignette CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="aa9df-113">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initializing the following parameters:</span></span>

<span data-ttu-id="aa9df-114">UINT widthInTexels</span><span class="sxs-lookup"><span data-stu-id="aa9df-114">UINT widthInTexels</span></span>

<span data-ttu-id="aa9df-115">UINT heightInTexels</span><span class="sxs-lookup"><span data-stu-id="aa9df-115">UINT heightInTexels</span></span>

<span data-ttu-id="aa9df-116">UINT depthInTexels</span><span class="sxs-lookup"><span data-stu-id="aa9df-116">UINT depthInTexels</span></span>

</dd> <dt>

<span data-ttu-id="aa9df-117">**\_& de forme de vignette const de l’opérateur D3D12 \_ () const**</span><span class="sxs-lookup"><span data-stu-id="aa9df-117">**operator const D3D12\_TILE\_SHAPE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="aa9df-118">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="aa9df-118">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa9df-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa9df-119">Requirements</span></span>



| <span data-ttu-id="aa9df-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa9df-120">Requirement</span></span> | <span data-ttu-id="aa9df-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa9df-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9df-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa9df-122">Header</span></span><br/> | <dl> <span data-ttu-id="aa9df-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa9df-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9df-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa9df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9df-125">**\_Forme de vignette D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="aa9df-125">**D3D12\_TILE\_SHAPE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[<span data-ttu-id="aa9df-126">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="aa9df-126">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





