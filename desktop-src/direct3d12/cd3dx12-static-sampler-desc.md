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
# <a name="cd3dx12_static_sampler_desc-structure"></a>CD3DX12, structure de l' \_ \_ échantillonneur statique \_

Une structure d’assistance pour permettre l’initialisation simple d’une structure d' [**\_ \_ échantillonneur \_ statique D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ - \_ échantillonneur statique \_ desc ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ échantillonneur statique CD3DX12 \_ \_ desc.

</dd> <dt>

**explicite CD3DX12 \_ explicite \_ \_ desc (const D3D12- \_ \_ échantillonneur statique \_ desc &o)**
</dt> <dd>

Crée une nouvelle instance d’un CD3DX12 \_ d' \_ échantillonneur statique \_ , initialisée avec le contenu d’une autre structure d' [**\_ \_ échantillonneur \_ statique D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

</dd> <dt>

**CD3DX12 \_ - \_ échantillonner statique \_ desc (uint shaderRegister, filtre filtre D3D12 \_ = D3D12 \_ Filtrer, D3D12 \_ \_ texture mode adresse \_ \_ Address = D3D12 \_ texture \_ \_ mode \_ , retour à la ligne, D3D12 mode adresse texture addressV \_ \_ \_ = D3D12 \_ mode adresse texture retour à \_ \_ \_ la ligne, D3D12 \_ texture \_ \_ mode AddressW = D3D12 \_ mode d' \_ adresse de texture \_ \_ Wrap, float MIPLODBIAS = 0, uint maxAnisotropy = 16, D3D12 \_ comparaison \_ Func comparisonFunc = D3D12 fonction \_ \_ de comparaison \_ inférieure \_ , D3D12 de \_ \_ bordure statique \_ couleur BORDERCOLOR = D3D12 \_ \_ de bordure statique \_ couleur \_ opaque \_ blanc, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ Visibility \_ All, uint registerSpace = 0**
</dt> <dd>

Crée une nouvelle instance d’un \_ \_ échantillonneur statique CD3DX12 \_ desc, en initialisant les paramètres suivants :

UINT shaderRegister

possibilité [**D3D12 \_ Filtre filtre =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtre \_ anisotrope

possibilité [**D3D12 \_ TEXTURE \_ \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) d’adresse de texture Address = D3D12 \_ mode d’adresse de texture \_ \_ \_

possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne

possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne

possibilité FLOAT mipLODBias = 0

possibilité UINT maxAnisotropy = 16

possibilité [**D3D12 \_ Fonction \_ de comparaison comparisonFunc =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) D3D12 de \_ comparaison \_ \_ moins \_ égale

possibilité [**D3D12 \_ \_ \_ Couleur de bordure statique**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statique couleur de \_ bordure \_ \_ opaque \_ blanc

possibilité FLOAT minLOD = 0. f

possibilité FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

possibilité [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ Visibility \_ All

possibilité UINT registerSpace = 0

</dd> <dt>

**static Inline init (D3D12 \_ statique \_ sampler \_ desc &SamplerDesc, uint shaderRegister, D3D12 filtre filter \_ = D3D12 \_ filtre \_ anisotrope, D3D12 \_ texture mode adresse Address \_ = D3D12 mode adresse texture retour à la ligne, D3D12 mode adresse texture \_ \_ \_ \_ \_ \_ \_ \_ addressV = \_ D3D12 \_ \_ mode adresse \_ de texture retour à la ligne, D3D12 \_ texture \_ \_ mode AddressW = D3D12 \_ mode d' \_ adresse de texture \_ \_ Wrap, float MIPLODBIAS = 0, uint maxAnisotropy = 16, D3D12 \_ comparaison \_ Func comparisonFunc = D3D12 fonction \_ \_ de comparaison \_ inférieure \_ , D3D12 de \_ \_ bordure statique \_ couleur BORDERCOLOR = D3D12 \_ \_ de bordure statique \_ couleur \_ opaque \_ blanc, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ Visibility \_ All, uint registerSpace = 0**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_ \_ Description de l’échantillonneur statique**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc

UINT shaderRegister

possibilité [**D3D12 \_ Filtre filtre =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtre \_ anisotrope

possibilité [**D3D12 \_ TEXTURE \_ \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) d’adresse de texture Address = D3D12 \_ mode d’adresse de texture \_ \_ \_

possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne

possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne

possibilité FLOAT mipLODBias = 0

possibilité UINT maxAnisotropy = 16

possibilité [**D3D12 \_ Fonction \_ de comparaison comparisonFunc =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) D3D12 de \_ comparaison \_ \_ moins \_ égale

possibilité [**D3D12 \_ \_ \_ Couleur de bordure statique**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statique couleur de \_ bordure \_ \_ opaque \_ blanc

possibilité FLOAT minLOD = 0. f

possibilité FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

possibilité [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ Visibility \_ All

possibilité UINT registerSpace = 0

</dd> <dt>

**Inline init (UINT shaderRegister, filtre filtre D3D12 \_ = D3D12 \_ Filter \_ anisotrope, D3D12 texture mode adresse Address- \_ \_ \_ D3D12 \_ texture \_ \_ mode \_ Wrap, D3D12 \_ \_ mode Address texture \_ mode ADDRESSV = D3D12 \_ \_ mode adresse texture \_ \_ Wrap, D3D12 \_ texture \_ \_ mode ADDRESSW = D3D12 \_ mode d' \_ adresse de texture \_ \_ Wrap, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ comparaison \_ Func comparisonFunc = D3D12 fonction \_ de comparaison \_ \_ inférieure \_ , D3D12 de \_ \_ bordure statique \_ couleur BorderColor = D3D12 \_ \_ de bordure statique \_ couleur \_ opaque \_ blanc, float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ Visibility \_ All, uint registerSpace = 0**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT shaderRegister

possibilité [**D3D12 \_ Filtre filtre =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtre \_ anisotrope

possibilité [**D3D12 \_ TEXTURE \_ \_ mode**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) d’adresse de texture Address = D3D12 \_ mode d’adresse de texture \_ \_ \_

possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne

possibilité [**D3D12 \_ \_ \_ Mode d’adresse de texture**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 mode d’adresse de \_ texture retour à \_ \_ \_ la ligne

possibilité FLOAT mipLODBias = 0

possibilité UINT maxAnisotropy = 16

possibilité [**D3D12 \_ Fonction \_ de comparaison comparisonFunc =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) D3D12 de \_ comparaison \_ \_ moins \_ égale

possibilité [**D3D12 \_ \_ \_ Couleur de bordure statique**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statique couleur de \_ bordure \_ \_ opaque \_ blanc

possibilité FLOAT minLOD = 0. f

possibilité FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

possibilité [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ Visibility \_ All

possibilité UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





