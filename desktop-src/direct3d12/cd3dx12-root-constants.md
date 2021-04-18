---
title: Structure CD3DX12_ROOT_CONSTANTS (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure de \_ \_ constantes racine D3D12.
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- Structure CD3DX12_ROOT_CONSTANTS
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520310"
---
# <a name="cd3dx12_root_constants-structure"></a><span data-ttu-id="cc316-104">CD3DX12 \_ , \_ structure de constantes racine</span><span class="sxs-lookup"><span data-stu-id="cc316-104">CD3DX12\_ROOT\_CONSTANTS structure</span></span>

<span data-ttu-id="cc316-105">Structure d’assistance pour permettre l’initialisation facile d’une structure [**de \_ \_ constantes racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="cc316-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc316-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc316-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="cc316-107">Membres</span><span class="sxs-lookup"><span data-stu-id="cc316-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc316-108">**CD3DX12 \_ \_ , constantes racine ()**</span><span class="sxs-lookup"><span data-stu-id="cc316-108">**CD3DX12\_ROOT\_CONSTANTS()**</span></span>
</dt> <dd>

<span data-ttu-id="cc316-109">Crée une nouvelle instance non initialisée d’une \_ constante racine CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="cc316-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_CONSTANTS.</span></span>

</dd> <dt>

<span data-ttu-id="cc316-110">**\_constantes racine CD3DX12 explicites \_ ( \_ constantes racine const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="cc316-110">**explicit CD3DX12\_ROOT\_CONSTANTS(const D3D12\_ROOT\_CONSTANTS &o)**</span></span>
</dt> <dd>

<span data-ttu-id="cc316-111">Crée une nouvelle instance de \_ \_ constantes racine CD3DX12, initialisée avec le contenu d’une autre structure de [**\_ \_ constantes racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="cc316-111">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initialized with the contents of another [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc316-112">**CD3DX12 \_ , \_ constantes racine (uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="cc316-112">**CD3DX12\_ROOT\_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="cc316-113">Crée une nouvelle instance de \_ \_ constantes racine CD3DX12, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="cc316-113">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initializing the following parameters:</span></span>

<span data-ttu-id="cc316-114">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="cc316-114">UINT num32BitValues</span></span>

<span data-ttu-id="cc316-115">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="cc316-115">UINT shaderRegister</span></span>

<span data-ttu-id="cc316-116">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="cc316-116">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="cc316-117">**Inline init (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="cc316-117">**inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="cc316-118">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="cc316-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="cc316-119">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="cc316-119">UINT num32BitValues</span></span>

<span data-ttu-id="cc316-120">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="cc316-120">UINT shaderRegister</span></span>

<span data-ttu-id="cc316-121">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="cc316-121">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="cc316-122">**static Inline init ( \_ \_ constantes racine D3D12 &ROOTCONSTANTS, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="cc316-122">**static inline Init(D3D12\_ROOT\_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="cc316-123">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="cc316-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="cc316-124">[**D3D12 \_ \_Constantes racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span><span class="sxs-lookup"><span data-stu-id="cc316-124">[**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span></span>

<span data-ttu-id="cc316-125">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="cc316-125">UINT num32BitValues</span></span>

<span data-ttu-id="cc316-126">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="cc316-126">UINT shaderRegister</span></span>

<span data-ttu-id="cc316-127">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="cc316-127">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc316-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc316-128">Requirements</span></span>



| <span data-ttu-id="cc316-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc316-129">Requirement</span></span> | <span data-ttu-id="cc316-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc316-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc316-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc316-131">Header</span></span><br/> | <dl> <span data-ttu-id="cc316-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc316-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc316-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc316-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc316-134">**\_ \_ Constantes racine D3D12**</span><span class="sxs-lookup"><span data-stu-id="cc316-134">**D3D12\_ROOT\_CONSTANTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[<span data-ttu-id="cc316-135">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="cc316-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





