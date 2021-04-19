---
title: Structure CD3DX12_ROOT_DESCRIPTOR (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ \_ structure de descripteurs racine D3D12.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- Structure CD3DX12_ROOT_DESCRIPTOR
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531578"
---
# <a name="cd3dx12_root_descriptor-structure"></a><span data-ttu-id="8157e-104">\_Structure du \_ descripteur racine CD3DX12</span><span class="sxs-lookup"><span data-stu-id="8157e-104">CD3DX12\_ROOT\_DESCRIPTOR structure</span></span>

<span data-ttu-id="8157e-105">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ descripteurs racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="8157e-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8157e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8157e-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="8157e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8157e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8157e-108">**\_Descripteur racine CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="8157e-108">**CD3DX12\_ROOT\_DESCRIPTOR()**</span></span>
</dt> <dd>

<span data-ttu-id="8157e-109">Crée une nouvelle instance non initialisée d’un \_ \_ descripteur racine CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="8157e-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR.</span></span>

</dd> <dt>

<span data-ttu-id="8157e-110">**\_descripteur racine CD3DX12 explicite \_ ( \_ descripteur racine const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="8157e-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR(const D3D12\_ROOT\_DESCRIPTOR &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8157e-111">Crée une nouvelle instance d’un \_ \_ descripteur racine CD3DX12, initialisée avec le contenu d’une autre structure de [**\_ \_ descripteur racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="8157e-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8157e-112">**\_Descripteur racine CD3DX12 \_ (uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="8157e-112">**CD3DX12\_ROOT\_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="8157e-113">Crée une nouvelle instance d’un \_ \_ descripteur racine CD3DX12, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8157e-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initializing the following parameters:</span></span>

<span data-ttu-id="8157e-114">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="8157e-114">UINT shaderRegister</span></span>

<span data-ttu-id="8157e-115">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8157e-115">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="8157e-116">**Inline init (UINT shaderRegister, UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="8157e-116">**inline Init(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="8157e-117">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8157e-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8157e-118">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="8157e-118">UINT shaderRegister</span></span>

<span data-ttu-id="8157e-119">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8157e-119">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="8157e-120">**static Inline init ( \_ \_ descripteur racine D3D12 &table, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="8157e-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="8157e-121">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8157e-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8157e-122">[**D3D12 \_ Tableau de &du \_ descripteur racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)</span><span class="sxs-lookup"><span data-stu-id="8157e-122">[**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &table</span></span>

<span data-ttu-id="8157e-123">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="8157e-123">UINT shaderRegister</span></span>

<span data-ttu-id="8157e-124">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8157e-124">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8157e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8157e-125">Requirements</span></span>



| <span data-ttu-id="8157e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8157e-126">Requirement</span></span> | <span data-ttu-id="8157e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8157e-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8157e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8157e-128">Header</span></span><br/> | <dl> <span data-ttu-id="8157e-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8157e-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8157e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8157e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8157e-131">**\_Descripteur racine D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="8157e-131">**D3D12\_ROOT\_DESCRIPTOR**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[<span data-ttu-id="8157e-132">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="8157e-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





