---
title: Structure CD3DX12_TILE_REGION_SIZE (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de taille de zone de vignette D3D12 \_ \_ .
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- Structure CD3DX12_TILE_REGION_SIZE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522568"
---
# <a name="cd3dx12_tile_region_size-structure"></a><span data-ttu-id="8678c-104">Structure de taille de la \_ zone de vignette CD3DX12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="8678c-104">CD3DX12\_TILE\_REGION\_SIZE structure</span></span>

<span data-ttu-id="8678c-105">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ taille de \_ zone \_ de vignette D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .</span><span class="sxs-lookup"><span data-stu-id="8678c-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8678c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8678c-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a><span data-ttu-id="8678c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8678c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8678c-108">**\_ \_ Taille de la zone de vignette CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="8678c-108">**CD3DX12\_TILE\_REGION\_SIZE()**</span></span>
</dt> <dd>

<span data-ttu-id="8678c-109">Crée une nouvelle instance non initialisée d’une \_ taille de zone de vignette CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8678c-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_REGION\_SIZE.</span></span>

</dd> <dt>

<span data-ttu-id="8678c-110">**\_ \_ taille de la zone de mosaïque CD3DX12 explicite \_ (taille de la zone de vignette const D3D12 \_ \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="8678c-110">**explicit CD3DX12\_TILE\_REGION\_SIZE(const D3D12\_TILE\_REGION\_SIZE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8678c-111">Crée une nouvelle instance d’une \_ taille de zone de vignette CD3DX12 \_ \_ , initialisée avec le contenu d’une autre structure de taille de [**\_ zone de vignette \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .</span><span class="sxs-lookup"><span data-stu-id="8678c-111">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initialized with the contents of another [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8678c-112">**\_ \_ Taille de la zone de vignette CD3DX12 \_ (uint NumTiles, bool useBox, uint Width, UINT16 hauteur, UInt16 depth)**</span><span class="sxs-lookup"><span data-stu-id="8678c-112">**CD3DX12\_TILE\_REGION\_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth)**</span></span>
</dt> <dd>

<span data-ttu-id="8678c-113">Crée une nouvelle instance d’une \_ taille de zone de vignette CD3DX12 \_ \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8678c-113">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initializing the following parameters:</span></span>

<span data-ttu-id="8678c-114">UINT numTiles</span><span class="sxs-lookup"><span data-stu-id="8678c-114">UINT numTiles</span></span>

<span data-ttu-id="8678c-115">BOOL useBox</span><span class="sxs-lookup"><span data-stu-id="8678c-115">BOOL useBox</span></span>

<span data-ttu-id="8678c-116">Largeur UINT</span><span class="sxs-lookup"><span data-stu-id="8678c-116">UINT width</span></span>

<span data-ttu-id="8678c-117">Hauteur de UINT16</span><span class="sxs-lookup"><span data-stu-id="8678c-117">UINT16 height</span></span>

<span data-ttu-id="8678c-118">Profondeur UINT16</span><span class="sxs-lookup"><span data-stu-id="8678c-118">UINT16 depth</span></span>

</dd> <dt>

<span data-ttu-id="8678c-119">**\_ \_ \_& taille de la zone de vignette D3D12 () const de l’opérateur const**</span><span class="sxs-lookup"><span data-stu-id="8678c-119">**operator const D3D12\_TILE\_REGION\_SIZE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="8678c-120">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="8678c-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8678c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8678c-121">Requirements</span></span>



| <span data-ttu-id="8678c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8678c-122">Requirement</span></span> | <span data-ttu-id="8678c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8678c-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8678c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8678c-124">Header</span></span><br/> | <dl> <span data-ttu-id="8678c-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8678c-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8678c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8678c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8678c-127">**Taille de la \_ zone de vignette D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8678c-127">**D3D12\_TILE\_REGION\_SIZE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[<span data-ttu-id="8678c-128">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="8678c-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





