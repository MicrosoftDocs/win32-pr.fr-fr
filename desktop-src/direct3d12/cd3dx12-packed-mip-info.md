---
title: Structure CD3DX12_PACKED_MIP_INFO (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure d’informations MIP D3D12 compressée \_ \_ .
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- Structure CD3DX12_PACKED_MIP_INFO
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539863"
---
# <a name="cd3dx12_packed_mip_info-structure"></a><span data-ttu-id="c7041-104">\_Structure d' \_ informations MIP CD3DX12 compressée \_</span><span class="sxs-lookup"><span data-stu-id="c7041-104">CD3DX12\_PACKED\_MIP\_INFO structure</span></span>

<span data-ttu-id="c7041-105">Structure d’assistance pour faciliter l’initialisation d’une structure d' [**\_ \_ \_ informations MIP D3D12 compressée**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .</span><span class="sxs-lookup"><span data-stu-id="c7041-105">A helper structure to enable easy initialization of a [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7041-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7041-106">Syntax</span></span>


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="c7041-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c7041-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7041-108">**\_Informations MIP CD3DX12 compressées \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="c7041-108">**CD3DX12\_PACKED\_MIP\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="c7041-109">Crée une nouvelle instance non initialisée d’une \_ information MIP CD3DX12 compressée \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c7041-109">Creates a new, uninitialized, instance of a CD3DX12\_PACKED\_MIP\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="c7041-110">**\_informations MIP CD3DX12 compressées explicites \_ \_ (const D3D12 \_ condensé \_ MIP \_ info &o)**</span><span class="sxs-lookup"><span data-stu-id="c7041-110">**explicit CD3DX12\_PACKED\_MIP\_INFO(const D3D12\_PACKED\_MIP\_INFO &o)**</span></span>
</dt> <dd>

<span data-ttu-id="c7041-111">Crée une instance d’une \_ information MIP CD3DX12 compressée \_ \_ , initialisée avec le contenu d’une autre structure d' [**\_ \_ \_ informations MIP compressée D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .</span><span class="sxs-lookup"><span data-stu-id="c7041-111">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initialized with the contents of another [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c7041-112">**\_Informations MIP CD3DX12 compressées \_ \_ (UINT8 NumStandardMips, UINT8 NumPackedMips, UINT NumTilesForPackedMips, uint startTileIndexInOverallResource)**</span><span class="sxs-lookup"><span data-stu-id="c7041-112">**CD3DX12\_PACKED\_MIP\_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="c7041-113">Crée une instance d’une \_ information MIP CD3DX12 compressée \_ \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c7041-113">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="c7041-114">UINT8 numStandardMips</span><span class="sxs-lookup"><span data-stu-id="c7041-114">UINT8 numStandardMips</span></span>

<span data-ttu-id="c7041-115">UINT8 numPackedMips</span><span class="sxs-lookup"><span data-stu-id="c7041-115">UINT8 numPackedMips</span></span>

<span data-ttu-id="c7041-116">UINT numTilesForPackedMips</span><span class="sxs-lookup"><span data-stu-id="c7041-116">UINT numTilesForPackedMips</span></span>

<span data-ttu-id="c7041-117">UINT startTileIndexInOverallResource</span><span class="sxs-lookup"><span data-stu-id="c7041-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="c7041-118">**const D3D12 \_ compressée \_ MIP \_ info& () const**</span><span class="sxs-lookup"><span data-stu-id="c7041-118">**operator const D3D12\_PACKED\_MIP\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="c7041-119">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="c7041-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7041-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7041-120">Requirements</span></span>



| <span data-ttu-id="c7041-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7041-121">Requirement</span></span> | <span data-ttu-id="c7041-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7041-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c7041-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7041-123">Header</span></span><br/> | <dl> <span data-ttu-id="c7041-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7041-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7041-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7041-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7041-126">**\_ \_ Informations MIP compressé \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="c7041-126">**D3D12\_PACKED\_MIP\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[<span data-ttu-id="c7041-127">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="c7041-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





