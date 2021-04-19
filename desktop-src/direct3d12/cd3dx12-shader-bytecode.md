---
title: Structure CD3DX12_SHADER_BYTECODE (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une structure de \_ bytecode de nuanceur D3D12 \_ .
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- Structure CD3DX12_SHADER_BYTECODE
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535791"
---
# <a name="cd3dx12_shader_bytecode-structure"></a><span data-ttu-id="a2f05-104">CD3DX12 \_ structure de bytecode du nuanceur \_</span><span class="sxs-lookup"><span data-stu-id="a2f05-104">CD3DX12\_SHADER\_BYTECODE structure</span></span>

<span data-ttu-id="a2f05-105">Une structure d’assistance pour faciliter l’initialisation d’une structure [**de \_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="a2f05-105">A helper structure to enable easy initialization of a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2f05-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2f05-106">Syntax</span></span>


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a><span data-ttu-id="a2f05-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a2f05-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2f05-108">**\_Bytecode du nuanceur CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="a2f05-108">**CD3DX12\_SHADER\_BYTECODE()**</span></span>
</dt> <dd>

<span data-ttu-id="a2f05-109">Crée une nouvelle instance non initialisée d’un \_ bytecode de nuanceur CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="a2f05-109">Creates a new, uninitialized, instance of a CD3DX12\_SHADER\_BYTECODE.</span></span>

</dd> <dt>

<span data-ttu-id="a2f05-110">**\_bytecode de nuanceur CD3DX12 explicite \_ ( \_ Pseudo-code du nuanceur const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="a2f05-110">**explicit CD3DX12\_SHADER\_BYTECODE(const D3D12\_SHADER\_BYTECODE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="a2f05-111">Crée une nouvelle instance d’un \_ bytecode de nuanceur CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="a2f05-111">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initialized with the contents of another [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a2f05-112">**\_Bytecode du nuanceur CD3DX12 \_ (ID3DBlob \* pShaderBlob)**</span><span class="sxs-lookup"><span data-stu-id="a2f05-112">**CD3DX12\_SHADER\_BYTECODE(ID3DBlob\* pShaderBlob)**</span></span>
</dt> <dd>

<span data-ttu-id="a2f05-113">Crée une nouvelle instance d’un \_ bytecode de nuanceur CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a2f05-113">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="a2f05-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob</span><span class="sxs-lookup"><span data-stu-id="a2f05-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))\* pShaderBlob</span></span>

</dd> <dt>

<span data-ttu-id="a2f05-115">**\_ \_ Bytecode de nuanceur CD3DX12 (const void \* \_ PShaderBytecode, size \_ T bytecodeLength)**</span><span class="sxs-lookup"><span data-stu-id="a2f05-115">**CD3DX12\_SHADER\_BYTECODE(const void\* \_pShaderBytecode, SIZE\_T bytecodeLength)**</span></span>
</dt> <dd>

<span data-ttu-id="a2f05-116">Crée une nouvelle instance d’un \_ bytecode de nuanceur CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a2f05-116">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="a2f05-117">void \* \_ pShaderBytecode</span><span class="sxs-lookup"><span data-stu-id="a2f05-117">void\* \_pShaderBytecode</span></span>

<span data-ttu-id="a2f05-118">TAILLE \_ T bytecodeLength</span><span class="sxs-lookup"><span data-stu-id="a2f05-118">SIZE\_T bytecodeLength</span></span>

</dd> <dt>

<span data-ttu-id="a2f05-119">**D3D12 \_ \_ () const, opérateur const,& bytecode de nuanceur**</span><span class="sxs-lookup"><span data-stu-id="a2f05-119">**operator const D3D12\_SHADER\_BYTECODE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="a2f05-120">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="a2f05-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2f05-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2f05-121">Requirements</span></span>



| <span data-ttu-id="a2f05-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2f05-122">Requirement</span></span> | <span data-ttu-id="a2f05-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2f05-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f05-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2f05-124">Header</span></span><br/> | <dl> <span data-ttu-id="a2f05-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2f05-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2f05-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2f05-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2f05-127">**\_Bytecode de nuanceur D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="a2f05-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[<span data-ttu-id="a2f05-128">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="a2f05-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

