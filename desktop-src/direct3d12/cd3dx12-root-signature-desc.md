---
title: Structure CD3DX12_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une \_ \_ structure DESC de signature racine D3D12 \_ .
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- Structure CD3DX12_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535842"
---
# <a name="cd3dx12_root_signature_desc-structure"></a><span data-ttu-id="9728e-104">CD3DX12 \_ \_ \_ structure Description de la signature racine</span><span class="sxs-lookup"><span data-stu-id="9728e-104">CD3DX12\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="9728e-105">Structure d’assistance pour permettre l’initialisation facile d’une structure [**\_ desc de \_ signature \_ racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="9728e-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9728e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9728e-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="9728e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9728e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9728e-108">**\_ \_ Description de la signature racine CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="9728e-108">**CD3DX12\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="9728e-109">Crée une nouvelle instance non initialisée d’une description de la \_ signature racine CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9728e-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="9728e-110">**\_Description de la signature racine CD3DX12 explicite \_ \_ desc (const D3D12 racine de la \_ \_ signature \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="9728e-110">**explicit CD3DX12\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="9728e-111">Crée une nouvelle instance d’une \_ Description de \_ signature racine CD3DX12 \_ , initialisée avec le contenu d’une autre structure [**\_ \_ \_ desc de signature D3D12 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="9728e-111">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with the contents of another [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9728e-112">**CD3DX12 \_ racine \_ signature \_ desc (uint numParameters, const D3D12 \_ racine \_ paramètre \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ \_ exemple statique \_ desc \* \_ pStaticSamplers = null, D3D12 indicateurs de \_ \_ signature racine \_ indicateurs = D3D12 \_ \_ indicateur signature \_ racine \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="9728e-112">**CD3DX12\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="9728e-113">Crée une nouvelle instance d’une \_ Description de \_ signature racine CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9728e-113">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="9728e-114">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="9728e-114">UINT numParameters</span></span>

<span data-ttu-id="9728e-115">[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="9728e-115">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="9728e-116">possibilité UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="9728e-116">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="9728e-117">possibilité [**D3D12 \_ \_Exemple statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="9728e-117">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="9728e-118">possibilité [**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="9728e-118">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="9728e-119">**\_ \_ Description de la signature racine CD3DX12 \_ ( \_ valeur par défaut CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="9728e-119">**CD3DX12\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="9728e-120">Crée une nouvelle instance d’une \_ Description de \_ signature racine CD3DX12 \_ , initialisée avec les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="9728e-120">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with default parameters.</span></span>

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

<span data-ttu-id="9728e-121">**Inline init (UINT numParameters, const D3D12 \_ racine \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ un \_ échantillonneur statique \_ desc \* \_ pStaticSamplers = null, \_ D3D12 \_ indicateurs de signature racine \_ indicateurs = D3D12 \_ indicateur de \_ signature racine \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="9728e-121">**inline Init(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="9728e-122">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9728e-122">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9728e-123">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="9728e-123">UINT numParameters</span></span>

<span data-ttu-id="9728e-124">[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="9728e-124">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="9728e-125">possibilité UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="9728e-125">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="9728e-126">possibilité [**D3D12 \_ \_Exemple statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="9728e-126">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="9728e-127">possibilité [**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="9728e-127">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="9728e-128">**static Inline init (D3D12 \_ racine de \_ SIGNATURE \_ desc &DESC, uint numParameters, const D3D12 \_ racine \_ \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ échantillon statique \_ \_ desc \* \_ pStaticSamplers = null, D3D12 indicateurs de \_ signature racine \_ \_ indicateurs = D3D12 \_ indicateur de signature racine \_ \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="9728e-128">**static inline Init(D3D12\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="9728e-129">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9728e-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9728e-130">[**D3D12 \_ Description de la \_ signature racine \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="9728e-130">[**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &desc</span></span>

<span data-ttu-id="9728e-131">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="9728e-131">UINT numParameters</span></span>

<span data-ttu-id="9728e-132">[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="9728e-132">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="9728e-133">possibilité UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="9728e-133">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="9728e-134">possibilité [**D3D12 \_ \_Exemple statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="9728e-134">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="9728e-135">possibilité [**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="9728e-135">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9728e-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9728e-136">Requirements</span></span>



| <span data-ttu-id="9728e-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9728e-137">Requirement</span></span> | <span data-ttu-id="9728e-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="9728e-138">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9728e-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="9728e-139">Header</span></span><br/> | <dl> <span data-ttu-id="9728e-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9728e-140"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9728e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9728e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9728e-142">**Description de la \_ signature racine D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9728e-142">**D3D12\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="9728e-143">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="9728e-143">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





