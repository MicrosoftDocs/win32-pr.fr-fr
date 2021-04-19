---
title: Structure CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une \_ \_ structure DESC de signature racine avec version D3D12 \_ \_ .
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- Structure CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538492"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a><span data-ttu-id="ffded-104">Structure de la description de la \_ \_ signature racine avec version CD3DX12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="ffded-104">CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="ffded-105">Une structure d’assistance pour faciliter l’initialisation d’une structure [**\_ \_ \_ \_ desc de signature racine avec version D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="ffded-105">A helper structure to enable easy initialization of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffded-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffded-106">Syntax</span></span>


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="ffded-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ffded-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ffded-108">**\_ \_ Description de la signature racine avec version CD3DX12 \_ \_ desc ()**</span><span class="sxs-lookup"><span data-stu-id="ffded-108">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-109">Crée une nouvelle instance non initialisée d’une description de la \_ signature racine avec version CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ffded-109">Creates a new, uninitialized, instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="ffded-110">**description explicite \_ de la \_ signature racine avec version CD3DX12 \_ \_ desc (const D3D12 \_ version de \_ \_ signature racine \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="ffded-110">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-111">Crée une nouvelle instance d’une \_ Description de la \_ signature racine avec version CD3DX12 \_ \_ , initialisée avec le contenu d’une structure [**\_ \_ \_ \_ desc de signature racine avec version D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="ffded-111">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ffded-112">**description explicite \_ de la \_ signature racine avec version CD3DX12 \_ \_ desc (const D3D12 racine de la \_ \_ signature \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="ffded-112">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-113">Crée une nouvelle instance d’une \_ Description de la \_ signature racine avec version CD3DX12 \_ \_ , initialisée avec le contenu d’une structure [**\_ \_ \_ desc de signature racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="ffded-113">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ffded-114">**\_Description de la signature racine avec version CD3DX12 explicite \_ \_ \_ desc (const D3D12 \_ racine \_ \_ DESC1 &o)**</span><span class="sxs-lookup"><span data-stu-id="ffded-114">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-115">Crée une nouvelle instance d’une \_ Description de la \_ signature racine avec version CD3DX12 \_ \_ , initialisée avec le contenu d’une structure [**\_ \_ \_ DESC1 de signature racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) .</span><span class="sxs-lookup"><span data-stu-id="ffded-115">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ffded-116">**\_ \_ Description de la signature racine avec version CD3DX12 \_ \_ desc (uint NUMPARAMETERS, const D3D12, \_ \_ paramètre racine \* \_ pParameters, uint numStaticSamplers = 0, const D3D12- \_ \_ échantillonneur statique \_ desc \* \_ pStaticSamplers = null, D3D12 \_ indicateurs de \_ signature racine \_ indicateurs = D3D12 \_ indicateur de \_ signature racine \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="ffded-116">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-117">Crée une nouvelle instance d’une \_ \_ Description de la signature racine avec version CD3DX12 \_ \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffded-117">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="ffded-118">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-118">UINT numParameters</span></span>

<span data-ttu-id="ffded-119">const [**D3D12 \_ \_ paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-119">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="ffded-120">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="ffded-120">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="ffded-121">const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="ffded-121">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="ffded-122">[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="ffded-122">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="ffded-123">**\_ \_ Description de la signature racine avec version CD3DX12 \_ \_ desc (uint NUMPARAMETERS, const D3D12 \_ racine \_ paramètre1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12- \_ \_ échantillonneur statique \_ desc \* \_ pStaticSamplers = null, D3D12 \_ indicateurs de \_ signature racine \_ indicateurs = D3D12 \_ indicateur de \_ signature racine \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="ffded-123">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-124">Crée une nouvelle instance d’une \_ \_ Description de la signature racine avec version CD3DX12 \_ \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffded-124">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="ffded-125">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-125">UINT numParameters</span></span>

<span data-ttu-id="ffded-126">const [**D3D12 \_ racine \_ paramètre1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-126">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="ffded-127">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="ffded-127">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="ffded-128">const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="ffded-128">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="ffded-129">[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="ffded-129">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="ffded-130">**\_ \_ Description de la signature racine avec version CD3DX12 \_ \_ desc ( \_ valeur par défaut CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="ffded-130">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-131">Crée une nouvelle instance d’une \_ \_ signature racine avec version \_ CD3DX12 \_ desc, initialisée avec les paramètres par défaut :</span><span class="sxs-lookup"><span data-stu-id="ffded-131">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the default parameters:</span></span>

<span data-ttu-id="ffded-132">UINT numParameters = 0</span><span class="sxs-lookup"><span data-stu-id="ffded-132">UINT numParameters = 0</span></span>

<span data-ttu-id="ffded-133">const [**D3D12 \_ racine \_ paramètre1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = null</span><span class="sxs-lookup"><span data-stu-id="ffded-133">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters = NULL</span></span>

<span data-ttu-id="ffded-134">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="ffded-134">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="ffded-135">const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="ffded-135">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="ffded-136">[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="ffded-136">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="ffded-137">**Init en ligne \_ 1 \_ 0 (uint numParameters, const D3D12 \_ , \_ paramètre racine \* \_ pParameters, uint NUMSTATICSAMPLERS = 0, const D3D12- \_ \_ échantillonneur statique \_ desc \* \_ PSTATICSAMPLERS = null, D3D12 \_ indicateurs de \_ signature racine \_ indicateurs = D3D12 \_ indicateur de signature racine \_ \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="ffded-137">**inline Init\_1\_0(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-138">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffded-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="ffded-139">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-139">UINT numParameters</span></span>

<span data-ttu-id="ffded-140">const [**D3D12 \_ \_ paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-140">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="ffded-141">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="ffded-141">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="ffded-142">const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="ffded-142">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="ffded-143">[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="ffded-143">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="ffded-144">**static Inline init \_ 1 \_ 0 (description de la \_ signature racine avec version D3D12 \_ \_ \_ desc &DESC, uint numParameters, const D3D12 \_ racine \_ \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ \_ échantillon statique \_ desc \* \_ pStaticSamplers = null, \_ indicateurs de signature racine D3D12 \_ \_ Flags = D3D12 \_ indicateur de signature racine \_ \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="ffded-144">**static inline Init\_1\_0(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-145">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffded-145">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="ffded-146">[**D3D12 \_ Description de \_ la \_ signature \_ racine avec version DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="ffded-146">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="ffded-147">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-147">UINT numParameters</span></span>

<span data-ttu-id="ffded-148">const [**D3D12 \_ \_ paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-148">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="ffded-149">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="ffded-149">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="ffded-150">const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="ffded-150">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="ffded-151">[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="ffded-151">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="ffded-152">**Init en ligne \_ 1 \_ 1 (uint numParameters, const D3D12 \_ racine \_ paramètre1 \* \_ pParameters, uint NUMSTATICSAMPLERS = 0, const D3D12 \_ \_ exemple statique \_ desc \* \_ PSTATICSAMPLERS = null, D3D12 indicateurs de \_ \_ signature racine \_ indicateurs = D3D12 \_ indicateur de \_ signature racine \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="ffded-152">**inline Init\_1\_1(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-153">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffded-153">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="ffded-154">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-154">UINT numParameters</span></span>

<span data-ttu-id="ffded-155">const [**D3D12 \_ racine \_ paramètre1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-155">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="ffded-156">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="ffded-156">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="ffded-157">const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="ffded-157">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="ffded-158">[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="ffded-158">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="ffded-159">**static Inline init \_ 1 \_ 1 (D3D12 de \_ signature racine avec version gérée \_ \_ \_ desc &DESC, uint numParameters, const D3D12 \_ racine \_ paramètre1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ \_ échantillon statique \_ desc \* \_ pStaticSamplers = null, \_ indicateurs de signature racine D3D12 \_ \_ indicateurs = D3D12 \_ indicateur de signature racine \_ \_ \_ aucun)**</span><span class="sxs-lookup"><span data-stu-id="ffded-159">**static inline Init\_1\_1(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="ffded-160">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffded-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="ffded-161">[**D3D12 \_ Description de \_ la \_ signature \_ racine avec version DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC</span><span class="sxs-lookup"><span data-stu-id="ffded-161">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="ffded-162">UINT numParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-162">UINT numParameters</span></span>

<span data-ttu-id="ffded-163">const [**D3D12 \_ racine \_ paramètre1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="ffded-163">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="ffded-164">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="ffded-164">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="ffded-165">const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null</span><span class="sxs-lookup"><span data-stu-id="ffded-165">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="ffded-166">[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="ffded-166">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffded-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffded-167">Requirements</span></span>



| <span data-ttu-id="ffded-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffded-168">Requirement</span></span> | <span data-ttu-id="ffded-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffded-169">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ffded-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffded-170">Header</span></span><br/> | <dl> <span data-ttu-id="ffded-171"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffded-171"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffded-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffded-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffded-173">**Description de la \_ signature racine avec version D3D12 \_ \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="ffded-173">**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="ffded-174">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="ffded-174">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





