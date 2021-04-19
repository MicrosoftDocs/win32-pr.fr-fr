---
title: Structure CD3DX12_TEXTURE_COPY_LOCATION (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure d' \_ emplacement de copie de texture D3D12 \_ \_ .
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- Structure CD3DX12_TEXTURE_COPY_LOCATION
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532424"
---
# <a name="cd3dx12_texture_copy_location-structure"></a><span data-ttu-id="91de9-104">CD3DX12 \_ structure de l’emplacement de copie de texture \_ \_</span><span class="sxs-lookup"><span data-stu-id="91de9-104">CD3DX12\_TEXTURE\_COPY\_LOCATION structure</span></span>

<span data-ttu-id="91de9-105">Structure d’assistance pour permettre l’initialisation facile d’une structure [**d' \_ \_ \_ emplacement de copie de texture D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .</span><span class="sxs-lookup"><span data-stu-id="91de9-105">A helper structure to enable easy initialization of a [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="91de9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91de9-106">Syntax</span></span>


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a><span data-ttu-id="91de9-107">Membres</span><span class="sxs-lookup"><span data-stu-id="91de9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="91de9-108">**\_ \_ \_ Emplacement de copie de texture CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="91de9-108">**CD3DX12\_TEXTURE\_COPY\_LOCATION()**</span></span>
</dt> <dd>

<span data-ttu-id="91de9-109">Crée une nouvelle instance non initialisée d’un \_ emplacement de copie de texture CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="91de9-109">Creates a new, uninitialized, instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION.</span></span>

</dd> <dt>

<span data-ttu-id="91de9-110">**\_ \_ emplacement de copie de texture CD3DX12 explicite \_ (const D3D12 \_ texture \_ \_ location &o)**</span><span class="sxs-lookup"><span data-stu-id="91de9-110">**explicit CD3DX12\_TEXTURE\_COPY\_LOCATION(const D3D12\_TEXTURE\_COPY\_LOCATION &o)**</span></span>
</dt> <dd>

<span data-ttu-id="91de9-111">Crée une nouvelle instance d’un \_ emplacement de copie de texture CD3DX12 \_ \_ , initialisée avec le contenu d’une autre structure d’emplacement de [**\_ copie de texture \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .</span><span class="sxs-lookup"><span data-stu-id="91de9-111">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initialized with the contents of another [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

</dd> <dt>

<span data-ttu-id="91de9-112">**\_ \_ \_ Emplacement de copie de texture CD3DX12 (ID3D12Resource \* pRes)**</span><span class="sxs-lookup"><span data-stu-id="91de9-112">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes)**</span></span>
</dt> <dd>

<span data-ttu-id="91de9-113">Crée une nouvelle instance d’un \_ emplacement de copie de texture CD3DX12 \_ \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="91de9-113">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="91de9-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Régisseur</span><span class="sxs-lookup"><span data-stu-id="91de9-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

</dd> <dt>

<span data-ttu-id="91de9-115">**\_ \_ \_ Emplacement de copie de texture CD3DX12 (ID3D12RESOURCE \* pRes, D3D12 a placé l’empreinte de sous- \_ \_ ressources \_ const& encombrement)**</span><span class="sxs-lookup"><span data-stu-id="91de9-115">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT const& Footprint)**</span></span>
</dt> <dd>

<span data-ttu-id="91de9-116">Crée une nouvelle instance d’un \_ emplacement de copie de texture CD3DX12 \_ \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="91de9-116">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="91de9-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Régisseur</span><span class="sxs-lookup"><span data-stu-id="91de9-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="91de9-118">[**D3D12 \_ Empreinte \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) des& CONSt imposées sur les sous-ressources</span><span class="sxs-lookup"><span data-stu-id="91de9-118">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& Footprint</span></span>

</dd> <dt>

<span data-ttu-id="91de9-119">**\_ \_ \_ Emplacement de copie de texture CD3DX12 (ID3D12RESOURCE \* pRes, uint Sub)**</span><span class="sxs-lookup"><span data-stu-id="91de9-119">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, UINT Sub)**</span></span>
</dt> <dd>

<span data-ttu-id="91de9-120">Crée une nouvelle instance d’un \_ emplacement de copie de texture CD3DX12 \_ \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="91de9-120">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="91de9-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Régisseur</span><span class="sxs-lookup"><span data-stu-id="91de9-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="91de9-122">UINT Sub</span><span class="sxs-lookup"><span data-stu-id="91de9-122">UINT Sub</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91de9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91de9-123">Requirements</span></span>



| <span data-ttu-id="91de9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91de9-124">Requirement</span></span> | <span data-ttu-id="91de9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="91de9-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="91de9-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="91de9-126">Header</span></span><br/> | <dl> <span data-ttu-id="91de9-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="91de9-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91de9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91de9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91de9-129">**\_Emplacement de \_ copie de texture D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="91de9-129">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[<span data-ttu-id="91de9-130">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="91de9-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





