---
title: Structure CD3DX12_SUBRESOURCE_FOOTPRINT (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une structure d’encombrement des sous- \_ ressources D3D12 \_ .
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- Structure CD3DX12_SUBRESOURCE_FOOTPRINT
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537238"
---
# <a name="cd3dx12_subresource_footprint-structure"></a><span data-ttu-id="17aa3-104">Structure d’encombrement des sous- \_ ressources CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="17aa3-104">CD3DX12\_SUBRESOURCE\_FOOTPRINT structure</span></span>

<span data-ttu-id="17aa3-105">Une structure d’assistance pour faciliter l’initialisation d’une structure [**d' \_ \_ Encombrement**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) des sous-ressources D3D12.</span><span class="sxs-lookup"><span data-stu-id="17aa3-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="17aa3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17aa3-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a><span data-ttu-id="17aa3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="17aa3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="17aa3-108">**\_Encombrement des sous-ressources CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="17aa3-108">**CD3DX12\_SUBRESOURCE\_FOOTPRINT()**</span></span>
</dt> <dd>

<span data-ttu-id="17aa3-109">Crée une nouvelle instance non initialisée d’un encombrement de sous- \_ ressources CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="17aa3-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT.</span></span>

</dd> <dt>

<span data-ttu-id="17aa3-110">**encombrement explicite des \_ sous-ressources CD3DX12 \_ (D3D12 des sous-ressources const \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="17aa3-110">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_SUBRESOURCE\_FOOTPRINT &o)**</span></span>
</dt> <dd>

<span data-ttu-id="17aa3-111">Crée une nouvelle instance d’un encombrement de sous- \_ ressources CD3DX12 \_ , initialisée avec le contenu d’une autre structure d’encombrement de sous- [**\_ ressources \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .</span><span class="sxs-lookup"><span data-stu-id="17aa3-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initialized with the contents of another [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

</dd> <dt>

<span data-ttu-id="17aa3-112">**\_Encombrement des sous-ressources CD3DX12 \_ ( \_ format de format dxgi, largeur UINT, hauteur uint, UINT Depth, uint rowPitch)**</span><span class="sxs-lookup"><span data-stu-id="17aa3-112">**CD3DX12\_SUBRESOURCE\_FOOTPRINT(DXGI\_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="17aa3-113">Crée une nouvelle instance d’un encombrement de sous- \_ ressources CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="17aa3-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="17aa3-114">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format</span><span class="sxs-lookup"><span data-stu-id="17aa3-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="17aa3-115">Largeur UINT</span><span class="sxs-lookup"><span data-stu-id="17aa3-115">UINT width</span></span>

<span data-ttu-id="17aa3-116">Hauteur UINT</span><span class="sxs-lookup"><span data-stu-id="17aa3-116">UINT height</span></span>

<span data-ttu-id="17aa3-117">Profondeur UINT</span><span class="sxs-lookup"><span data-stu-id="17aa3-117">UINT depth</span></span>

<span data-ttu-id="17aa3-118">UINT rowPitch</span><span class="sxs-lookup"><span data-stu-id="17aa3-118">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="17aa3-119">**encombrement explicite des \_ sous-ressources CD3DX12 \_ (CONSt D3D12 \_ resource \_ desc& resDesc, uint rowPitch)**</span><span class="sxs-lookup"><span data-stu-id="17aa3-119">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_RESOURCE\_DESC& resDesc, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="17aa3-120">Crée une nouvelle instance d’un encombrement de sous- \_ ressources CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="17aa3-120">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="17aa3-121">[**D3D12 \_ \_Description**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) de la ressource& resDesc</span><span class="sxs-lookup"><span data-stu-id="17aa3-121">[**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc</span></span>

<span data-ttu-id="17aa3-122">UINT rowPitch</span><span class="sxs-lookup"><span data-stu-id="17aa3-122">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="17aa3-123">**const D3D12 \_ sous-ressource \_ encombrement& () const**</span><span class="sxs-lookup"><span data-stu-id="17aa3-123">**operator const D3D12\_SUBRESOURCE\_FOOTPRINT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="17aa3-124">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="17aa3-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17aa3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17aa3-125">Requirements</span></span>



| <span data-ttu-id="17aa3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17aa3-126">Requirement</span></span> | <span data-ttu-id="17aa3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="17aa3-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="17aa3-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="17aa3-128">Header</span></span><br/> | <dl> <span data-ttu-id="17aa3-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="17aa3-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17aa3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17aa3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17aa3-131">**Encombrement des sous- \_ ressources D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="17aa3-131">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[<span data-ttu-id="17aa3-132">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="17aa3-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

