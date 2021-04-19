---
title: Structure CD3DX12_ROOT_DESCRIPTOR_TABLE (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de table de \_ descripteurs racine D3D12 \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- Structure CD3DX12_ROOT_DESCRIPTOR_TABLE
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520309"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a><span data-ttu-id="8e956-104">\_Structure de \_ table de descripteurs racine CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="8e956-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE structure</span></span>

<span data-ttu-id="8e956-105">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ \_ table de descripteurs racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .</span><span class="sxs-lookup"><span data-stu-id="8e956-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e956-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e956-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="8e956-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8e956-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8e956-108">**\_ \_ Tableau de descripteurs racine CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="8e956-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE()**</span></span>
</dt> <dd>

<span data-ttu-id="8e956-109">Crée une nouvelle instance non initialisée d’une \_ \_ table de descripteurs racine CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="8e956-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE.</span></span>

</dd> <dt>

<span data-ttu-id="8e956-110">**\_ \_ table de descripteurs racine CD3DX12 explicite \_ ( \_ table de descripteur racine const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="8e956-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(const D3D12\_ROOT\_DESCRIPTOR\_TABLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8e956-111">Crée une nouvelle instance d’une \_ table de \_ descripteurs racine CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ \_ table de descripteurs racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .</span><span class="sxs-lookup"><span data-stu-id="8e956-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8e956-112">**CD3DX12 \_ \_ table descripteur racine \_ (uint numDescriptorRanges, const D3D12 \_ descripteur \_ Range \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="8e956-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="8e956-113">Crée une nouvelle instance d’une \_ table de \_ descripteurs racine CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e956-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initializing the following parameters:</span></span>

<span data-ttu-id="8e956-114">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8e956-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="8e956-115">[**D3D12 \_ \_Plage de descripteurs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8e956-115">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="8e956-116">**Inline init (UINT numDescriptorRanges, const D3D12 \_ descripteur \_ Range \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="8e956-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="8e956-117">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e956-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8e956-118">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8e956-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="8e956-119">[**D3D12 \_ \_Plage de descripteurs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8e956-119">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="8e956-120">**static Inline init ( \_ \_ table descripteur racine D3D12 \_ &RootDescriptorTable, uint numDescriptorRanges, const D3D12 \_ descripteur \_ Range \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="8e956-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="8e956-121">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e956-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8e956-122">[**D3D12 \_ \_ \_ Tableau du descripteur racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="8e956-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span></span>

<span data-ttu-id="8e956-123">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8e956-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="8e956-124">[**D3D12 \_ \_Plage de descripteurs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8e956-124">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e956-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e956-125">Requirements</span></span>



| <span data-ttu-id="8e956-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e956-126">Requirement</span></span> | <span data-ttu-id="8e956-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e956-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8e956-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e956-128">Header</span></span><br/> | <dl> <span data-ttu-id="8e956-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e956-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e956-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e956-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e956-131">**\_Tableau de \_ descripteurs racine D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="8e956-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[<span data-ttu-id="8e956-132">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="8e956-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





