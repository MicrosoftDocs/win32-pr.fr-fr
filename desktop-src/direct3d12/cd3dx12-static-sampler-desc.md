---
title: Structure CD3DX12_STATIC_SAMPLER_DESC (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation simple d’une \_ structure d' \_ échantillonneur statique D3D12 \_ .
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- Structure CD3DX12_STATIC_SAMPLER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538314"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a><span data-ttu-id="c65d4-104">CD3DX12, structure de l' \_ \_ échantillonneur statique \_</span><span class="sxs-lookup"><span data-stu-id="c65d4-104">CD3DX12\_STATIC\_SAMPLER\_DESC structure</span></span>

<span data-ttu-id="c65d4-105">Une structure d’assistance pour permettre l’initialisation simple d’une structure d' [**\_ \_ échantillonneur \_ statique D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="c65d4-105">A helper structure to enable easy initialization of a [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c65d4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c65d4-106">Syntax</span></span>


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="c65d4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c65d4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c65d4-108">**CD3DX12 \_ - \_ échantillonneur statique \_ desc ()**</span><span class="sxs-lookup"><span data-stu-id="c65d4-108">**CD3DX12\_STATIC\_SAMPLER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="c65d4-109">Crée une nouvelle instance non initialisée d’un \_ échantillonneur statique CD3DX12 \_ \_ desc.</span><span class="sxs-lookup"><span data-stu-id="c65d4-109">Creates a new, uninitialized, instance of a CD3DX12\_STATIC\_SAMPLER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="c65d4-110">**explicite CD3DX12 \_ explicite \_ \_ desc (const D3D12- \_ \_ échantillonneur statique \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="c65d4-110">**explicit CD3DX12\_STATIC\_SAMPLER\_DESC(const D3D12\_STATIC\_SAMPLER\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="c65d4-111">Crée une nouvelle instance d’un CD3DX12 \_ d' \_ échantillonneur statique \_ , initialisée avec le contenu d’une autre structure d' [**\_ \_ échantillonneur \_ statique D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="c65d4-111">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initialized with the contents of another [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c65d4-112">**CD3DX12 \_ - \_ échantillonner statique \_ desc (uint shaderRegister, filtre filtre D3D12 \_ = D3D12 \_ Filtrer, D3D12 \_ \_ texture mode adresse \_ \_ Address = D3D12 \_ texture \_ \_ mode \_ , retour à la ligne, D3D12 mode adresse texture addressV \_ \_ \_ = D3D12 \_ mode adresse texture retour à \_ \_ \_ la ligne, D3D12 \_ texture \_ \_ mode AddressW = D3D12 \_ mode d' \_ adresse de texture \_ \_ Wrap, float MIPLODBIAS = 0, uint maxAnisotropy = 16, D3D12 \_ comparaison \_ Func comparisonFunc = D3D12 fonction \_ \_ de comparaison \_ inférieure \_ , D3D12 de \_ \_ bordure statique \_ couleur BORDERCOLOR = D3D12 \_ \_ de bordure statique \_ couleur \_ opaque \_ blanc, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ Visibility \_ All, uint registerSpace = 0**</span><span class="sxs-lookup"><span data-stu-id="c65d4-112">**CD3DX12\_STATIC\_SAMPLER\_DESC(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="c65d4-113">Crée une nouvelle instance d’un \_ \_ échantillonneur statique CD3DX12 \_ desc, en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c65d4-113">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="c65d4-114">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="c65d4-114">UINT shaderRegister</span></span>

<span data-ttu-id="c65d4-115">possibilité [**D3D12 \_ Filtre filtre =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtre \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="c65d4-115">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="c65d4-116">possibilité [**D3D12 \_ TEXTURE \_ \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) d’adresse de texture Address = D3D12 \_ mode d’adresse de texture \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c65d4-116">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="c65d4-117">possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne</span><span class="sxs-lookup"><span data-stu-id="c65d4-117">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="c65d4-118">possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne</span><span class="sxs-lookup"><span data-stu-id="c65d4-118">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="c65d4-119">possibilité FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="c65d4-119">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="c65d4-120">possibilité UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="c65d4-120">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="c65d4-121">possibilité [**D3D12 \_ Fonction \_ de comparaison comparisonFunc =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) D3D12 de \_ comparaison \_ \_ moins \_ égale</span><span class="sxs-lookup"><span data-stu-id="c65d4-121">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="c65d4-122">possibilité [**D3D12 \_ \_ \_ Couleur de bordure statique**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statique couleur de \_ bordure \_ \_ opaque \_ blanc</span><span class="sxs-lookup"><span data-stu-id="c65d4-122">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="c65d4-123">possibilité FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="c65d4-123">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="c65d4-124">possibilité FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="c65d4-124">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="c65d4-125">possibilité [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ Visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="c65d4-125">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="c65d4-126">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="c65d4-126">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="c65d4-127">**static Inline init (D3D12 \_ statique \_ sampler \_ desc &SamplerDesc, uint shaderRegister, D3D12 filtre filter \_ = D3D12 \_ filtre \_ anisotrope, D3D12 \_ texture mode adresse Address \_ = D3D12 mode adresse texture retour à la ligne, D3D12 mode adresse texture \_ \_ \_ \_ \_ \_ \_ \_ addressV = \_ D3D12 \_ \_ mode adresse \_ de texture retour à la ligne, D3D12 \_ texture \_ \_ mode AddressW = D3D12 \_ mode d' \_ adresse de texture \_ \_ Wrap, float MIPLODBIAS = 0, uint maxAnisotropy = 16, D3D12 \_ comparaison \_ Func comparisonFunc = D3D12 fonction \_ \_ de comparaison \_ inférieure \_ , D3D12 de \_ \_ bordure statique \_ couleur BORDERCOLOR = D3D12 \_ \_ de bordure statique \_ couleur \_ opaque \_ blanc, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ Visibility \_ All, uint registerSpace = 0**</span><span class="sxs-lookup"><span data-stu-id="c65d4-127">**static inline Init(D3D12\_STATIC\_SAMPLER\_DESC &samplerDesc, UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="c65d4-128">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c65d4-128">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="c65d4-129">[**D3D12 \_ \_ \_ Description de l’échantillonneur statique**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span><span class="sxs-lookup"><span data-stu-id="c65d4-129">[**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span></span>

<span data-ttu-id="c65d4-130">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="c65d4-130">UINT shaderRegister</span></span>

<span data-ttu-id="c65d4-131">possibilité [**D3D12 \_ Filtre filtre =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtre \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="c65d4-131">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="c65d4-132">possibilité [**D3D12 \_ TEXTURE \_ \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) d’adresse de texture Address = D3D12 \_ mode d’adresse de texture \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c65d4-132">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="c65d4-133">possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne</span><span class="sxs-lookup"><span data-stu-id="c65d4-133">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="c65d4-134">possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne</span><span class="sxs-lookup"><span data-stu-id="c65d4-134">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="c65d4-135">possibilité FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="c65d4-135">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="c65d4-136">possibilité UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="c65d4-136">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="c65d4-137">possibilité [**D3D12 \_ Fonction \_ de comparaison comparisonFunc =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) D3D12 de \_ comparaison \_ \_ moins \_ égale</span><span class="sxs-lookup"><span data-stu-id="c65d4-137">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="c65d4-138">possibilité [**D3D12 \_ \_ \_ Couleur de bordure statique**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statique couleur de \_ bordure \_ \_ opaque \_ blanc</span><span class="sxs-lookup"><span data-stu-id="c65d4-138">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="c65d4-139">possibilité FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="c65d4-139">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="c65d4-140">possibilité FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="c65d4-140">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="c65d4-141">possibilité [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ Visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="c65d4-141">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="c65d4-142">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="c65d4-142">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="c65d4-143">**Inline init (UINT shaderRegister, filtre filtre D3D12 \_ = D3D12 \_ Filter \_ anisotrope, D3D12 texture mode adresse Address- \_ \_ \_ D3D12 \_ texture \_ \_ mode \_ Wrap, D3D12 \_ \_ mode Address texture \_ mode ADDRESSV = D3D12 \_ \_ mode adresse texture \_ \_ Wrap, D3D12 \_ texture \_ \_ mode ADDRESSW = D3D12 \_ mode d' \_ adresse de texture \_ \_ Wrap, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ comparaison \_ Func comparisonFunc = D3D12 fonction \_ de comparaison \_ \_ inférieure \_ , D3D12 de \_ \_ bordure statique \_ couleur BorderColor = D3D12 \_ \_ de bordure statique \_ couleur \_ opaque \_ blanc, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ Visibility \_ All, uint registerSpace = 0**</span><span class="sxs-lookup"><span data-stu-id="c65d4-143">**inline Init(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="c65d4-144">Spécifie une fonction qui initialise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="c65d4-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="c65d4-145">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="c65d4-145">UINT shaderRegister</span></span>

<span data-ttu-id="c65d4-146">possibilité [**D3D12 \_ Filtre filtre =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtre \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="c65d4-146">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="c65d4-147">possibilité [**D3D12 \_ TEXTURE \_ \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) d’adresse de texture Address = D3D12 \_ mode d’adresse de texture \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c65d4-147">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="c65d4-148">possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne</span><span class="sxs-lookup"><span data-stu-id="c65d4-148">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="c65d4-149">possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne</span><span class="sxs-lookup"><span data-stu-id="c65d4-149">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="c65d4-150">possibilité FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="c65d4-150">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="c65d4-151">possibilité UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="c65d4-151">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="c65d4-152">possibilité [**D3D12 \_ Fonction \_ de comparaison comparisonFunc =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) D3D12 de \_ comparaison \_ \_ moins \_ égale</span><span class="sxs-lookup"><span data-stu-id="c65d4-152">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="c65d4-153">possibilité [**D3D12 \_ \_ \_ Couleur de bordure statique**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statique couleur de \_ bordure \_ \_ opaque \_ blanc</span><span class="sxs-lookup"><span data-stu-id="c65d4-153">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="c65d4-154">possibilité FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="c65d4-154">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="c65d4-155">possibilité FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="c65d4-155">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="c65d4-156">possibilité [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ Visibility \_ All</span><span class="sxs-lookup"><span data-stu-id="c65d4-156">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="c65d4-157">possibilité UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="c65d4-157">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c65d4-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c65d4-158">Requirements</span></span>



| <span data-ttu-id="c65d4-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c65d4-159">Requirement</span></span> | <span data-ttu-id="c65d4-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="c65d4-160">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c65d4-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="c65d4-161">Header</span></span><br/> | <dl> <span data-ttu-id="c65d4-162"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c65d4-162"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c65d4-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c65d4-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c65d4-164">**D3D12 \_ - \_ échantillonneur statique \_ desc**</span><span class="sxs-lookup"><span data-stu-id="c65d4-164">**D3D12\_STATIC\_SAMPLER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[<span data-ttu-id="c65d4-165">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="c65d4-165">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





