---
title: Structure CD3DX12_VIEWPORT (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de fenêtre d’affichage D3D12.
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- Structure CD3DX12_VIEWPORT
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535206"
---
# <a name="cd3dx12_viewport-structure"></a><span data-ttu-id="4307c-104">Structure de la \_ fenêtre d’affichage CD3DX12</span><span class="sxs-lookup"><span data-stu-id="4307c-104">CD3DX12\_VIEWPORT structure</span></span>

<span data-ttu-id="4307c-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="4307c-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4307c-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="4307c-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4307c-107">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ fenêtre d’affichage D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) .</span><span class="sxs-lookup"><span data-stu-id="4307c-107">A helper structure to enable easy initialization of a [**D3D12\_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4307c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4307c-108">Syntax</span></span>


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a><span data-ttu-id="4307c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="4307c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4307c-110">**CD3DX12 \_ VIEWPORT ()**</span><span class="sxs-lookup"><span data-stu-id="4307c-110">**CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="4307c-111">Crée une nouvelle instance non initialisée d’une \_ fenêtre d’affichage CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="4307c-111">Creates a new, uninitialized, instance of a CD3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="4307c-112">**Viewport CD3DX12 explicite \_ (fenêtre d’affichage const D3D12 \_& o)**</span><span class="sxs-lookup"><span data-stu-id="4307c-112">**explicit CD3DX12\_VIEWPORT(const D3D12\_VIEWPORT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="4307c-113">Crée une nouvelle instance d’une \_ fenêtre d’affichage CD3DX12, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4307c-113">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="4307c-114">& de la fenêtre d’affichage const D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="4307c-114">const D3D12\_VIEWPORT& o</span></span>

</dd> <dt>

<span data-ttu-id="4307c-115">**VIEWPORT CD3DX12 explicite \_ (float topLeftX, float point Left, Floating, float height, float minDepth = D3D12 \_ Min \_ profondeur, float maxdepth = D3D12 \_ Max \_ depth)**</span><span class="sxs-lookup"><span data-stu-id="4307c-115">**explicit CD3DX12\_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="4307c-116">Crée une nouvelle instance d’une \_ fenêtre d’affichage CD3DX12, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4307c-116">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="4307c-117">TopLeftX FLOAT</span><span class="sxs-lookup"><span data-stu-id="4307c-117">FLOAT topLeftX</span></span>

<span data-ttu-id="4307c-118">Virgule flottante à gauche</span><span class="sxs-lookup"><span data-stu-id="4307c-118">FLOAT topLeftY</span></span>

<span data-ttu-id="4307c-119">Largeur de la virgule flottante</span><span class="sxs-lookup"><span data-stu-id="4307c-119">FLOAT width</span></span>

<span data-ttu-id="4307c-120">Hauteur de flotte</span><span class="sxs-lookup"><span data-stu-id="4307c-120">FLOAT height</span></span>

<span data-ttu-id="4307c-121">FLOAT minDepth = D3D12 \_ Min \_ Depth</span><span class="sxs-lookup"><span data-stu-id="4307c-121">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="4307c-122">FLOAT maxDepth = D3D12 \_ Max \_ Depth</span><span class="sxs-lookup"><span data-stu-id="4307c-122">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="4307c-123">**VIEWPORT CD3DX12 explicite \_ (ID3D12Resource \* présource, uint mipSlice = 0, float topLeftX = 0.0 f, float Left = 0.0 f, float MINDEPTH = D3D12 \_ Min \_ Depth, float maxdepth = D3D12 \_ Max \_ depth)**</span><span class="sxs-lookup"><span data-stu-id="4307c-123">**explicit CD3DX12\_VIEWPORT(ID3D12Resource\* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="4307c-124">Crée une nouvelle instance d’une \_ fenêtre d’affichage CD3DX12, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="4307c-124">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="4307c-125">ID3D12Resource préversion \*</span><span class="sxs-lookup"><span data-stu-id="4307c-125">ID3D12Resource\* pResource</span></span>

<span data-ttu-id="4307c-126">UINT mipSlice = 0</span><span class="sxs-lookup"><span data-stu-id="4307c-126">UINT mipSlice = 0</span></span>

<span data-ttu-id="4307c-127">FLOAT topLeftX = 0.0 f</span><span class="sxs-lookup"><span data-stu-id="4307c-127">FLOAT topLeftX = 0.0f</span></span>

<span data-ttu-id="4307c-128">FLOAT Left = 0.0 f</span><span class="sxs-lookup"><span data-stu-id="4307c-128">FLOAT topLeftY = 0.0f</span></span>

<span data-ttu-id="4307c-129">FLOAT minDepth = D3D12 \_ Min \_ Depth</span><span class="sxs-lookup"><span data-stu-id="4307c-129">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="4307c-130">FLOAT maxDepth = D3D12 \_ Max \_ Depth</span><span class="sxs-lookup"><span data-stu-id="4307c-130">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="4307c-131">**~ CD3DX12 \_ VIEWPORT ()**</span><span class="sxs-lookup"><span data-stu-id="4307c-131">**~CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="4307c-132">Détruit une instance d’une fenêtre d' \_ affichage D3DX12.</span><span class="sxs-lookup"><span data-stu-id="4307c-132">Destroys an instance of a D3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="4307c-133">**\_const D3D12 fenêtre d’affichage& () const**</span><span class="sxs-lookup"><span data-stu-id="4307c-133">**operator const D3D12\_VIEWPORT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="4307c-134">Définit le & opérateur de passage par référence pour le type de structure parent.</span><span class="sxs-lookup"><span data-stu-id="4307c-134">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4307c-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4307c-135">Requirements</span></span>



| <span data-ttu-id="4307c-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4307c-136">Requirement</span></span> | <span data-ttu-id="4307c-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="4307c-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4307c-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="4307c-138">Header</span></span><br/> | <dl> <span data-ttu-id="4307c-139"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4307c-139"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4307c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4307c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4307c-141">**D3D12 \_ VIEWPORT**</span><span class="sxs-lookup"><span data-stu-id="4307c-141">**D3D12\_VIEWPORT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[<span data-ttu-id="4307c-142">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="4307c-142">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





