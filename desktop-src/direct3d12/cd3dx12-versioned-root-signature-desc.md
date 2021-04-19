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
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a>Structure de la description de la \_ \_ signature racine avec version CD3DX12 \_ \_

Une structure d’assistance pour faciliter l’initialisation d’une structure [**\_ \_ \_ \_ desc de signature racine avec version D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

## <a name="syntax"></a>Syntaxe


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



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ Description de la signature racine avec version CD3DX12 \_ \_ desc ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une description de la \_ signature racine avec version CD3DX12 \_ \_ \_ .

</dd> <dt>

**description explicite \_ de la \_ signature racine avec version CD3DX12 \_ \_ desc (const D3D12 \_ version de \_ \_ signature racine \_ desc &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description de la \_ signature racine avec version CD3DX12 \_ \_ , initialisée avec le contenu d’une structure [**\_ \_ \_ \_ desc de signature racine avec version D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

</dd> <dt>

**description explicite \_ de la \_ signature racine avec version CD3DX12 \_ \_ desc (const D3D12 racine de la \_ \_ signature \_ desc &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description de la \_ signature racine avec version CD3DX12 \_ \_ , initialisée avec le contenu d’une structure [**\_ \_ \_ desc de signature racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

</dd> <dt>

**\_Description de la signature racine avec version CD3DX12 explicite \_ \_ \_ desc (const D3D12 \_ racine \_ \_ DESC1 &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description de la \_ signature racine avec version CD3DX12 \_ \_ , initialisée avec le contenu d’une structure [**\_ \_ \_ DESC1 de signature racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) .

</dd> <dt>

**\_ \_ Description de la signature racine avec version CD3DX12 \_ \_ desc (uint NUMPARAMETERS, const D3D12, \_ \_ paramètre racine \* \_ pParameters, uint numStaticSamplers = 0, const D3D12- \_ \_ échantillonneur statique \_ desc \* \_ pStaticSamplers = null, D3D12 \_ indicateurs de \_ signature racine \_ indicateurs = D3D12 \_ indicateur de \_ signature racine \_ \_ aucun)**
</dt> <dd>

Crée une nouvelle instance d’une \_ \_ Description de la signature racine avec version CD3DX12 \_ \_ , en initialisant les paramètres suivants :

UINT numParameters

const [**D3D12 \_ \_ paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun

</dd> <dt>

**\_ \_ Description de la signature racine avec version CD3DX12 \_ \_ desc (uint NUMPARAMETERS, const D3D12 \_ racine \_ paramètre1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12- \_ \_ échantillonneur statique \_ desc \* \_ pStaticSamplers = null, D3D12 \_ indicateurs de \_ signature racine \_ indicateurs = D3D12 \_ indicateur de \_ signature racine \_ \_ aucun)**
</dt> <dd>

Crée une nouvelle instance d’une \_ \_ Description de la signature racine avec version CD3DX12 \_ \_ , en initialisant les paramètres suivants :

UINT numParameters

const [**D3D12 \_ racine \_ paramètre1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun

</dd> <dt>

**\_ \_ Description de la signature racine avec version CD3DX12 \_ \_ desc ( \_ valeur par défaut CD3DX12)**
</dt> <dd>

Crée une nouvelle instance d’une \_ \_ signature racine avec version \_ CD3DX12 \_ desc, initialisée avec les paramètres par défaut :

UINT numParameters = 0

const [**D3D12 \_ racine \_ paramètre1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = null

UINT numStaticSamplers = 0

const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun

</dd> <dt>

**Init en ligne \_ 1 \_ 0 (uint numParameters, const D3D12 \_ , \_ paramètre racine \* \_ pParameters, uint NUMSTATICSAMPLERS = 0, const D3D12- \_ \_ échantillonneur statique \_ desc \* \_ PSTATICSAMPLERS = null, D3D12 \_ indicateurs de \_ signature racine \_ indicateurs = D3D12 \_ indicateur de signature racine \_ \_ \_ aucun)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT numParameters

const [**D3D12 \_ \_ paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun

</dd> <dt>

**static Inline init \_ 1 \_ 0 (description de la \_ signature racine avec version D3D12 \_ \_ \_ desc &DESC, uint numParameters, const D3D12 \_ racine \_ \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ \_ échantillon statique \_ desc \* \_ pStaticSamplers = null, \_ indicateurs de signature racine D3D12 \_ \_ Flags = D3D12 \_ indicateur de signature racine \_ \_ \_ aucun)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ Description de \_ la \_ signature \_ racine avec version DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC

UINT numParameters

const [**D3D12 \_ \_ paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun

</dd> <dt>

**Init en ligne \_ 1 \_ 1 (uint numParameters, const D3D12 \_ racine \_ paramètre1 \* \_ pParameters, uint NUMSTATICSAMPLERS = 0, const D3D12 \_ \_ exemple statique \_ desc \* \_ PSTATICSAMPLERS = null, D3D12 indicateurs de \_ \_ signature racine \_ indicateurs = D3D12 \_ indicateur de \_ signature racine \_ \_ aucun)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT numParameters

const [**D3D12 \_ racine \_ paramètre1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun

</dd> <dt>

**static Inline init \_ 1 \_ 1 (D3D12 de \_ signature racine avec version gérée \_ \_ \_ desc &DESC, uint numParameters, const D3D12 \_ racine \_ paramètre1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ \_ échantillon statique \_ desc \* \_ pStaticSamplers = null, \_ indicateurs de signature racine D3D12 \_ \_ indicateurs = D3D12 \_ indicateur de signature racine \_ \_ \_ aucun)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ Description de \_ la \_ signature \_ racine avec version DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &DESC

UINT numParameters

const [**D3D12 \_ racine \_ paramètre1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ - \_ échantillonneur statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

[**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Description de la \_ signature racine avec version D3D12 \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





