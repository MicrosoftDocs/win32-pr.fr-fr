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
ms.openlocfilehash: 3fb68acfbe76c4a32e0549da97fbe9dc3c8daae23fe72fc4757f3b840421da22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988389"
---
# <a name="cd3dx12_root_signature_desc-structure"></a>CD3DX12 \_ \_ \_ structure Description de la signature racine

Structure d’assistance pour permettre l’initialisation facile d’une structure [**\_ desc de \_ signature \_ racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

## <a name="syntax"></a>Syntaxe


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



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ Description de la signature racine CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une description de la \_ signature racine CD3DX12 \_ \_ .

</dd> <dt>

**\_Description de la signature racine CD3DX12 explicite \_ \_ desc (const D3D12 racine de la \_ \_ signature \_ desc &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description de \_ signature racine CD3DX12 \_ , initialisée avec le contenu d’une autre structure [**\_ \_ \_ desc de signature D3D12 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

</dd> <dt>

**CD3DX12 \_ racine \_ signature \_ desc (uint numParameters, const D3D12 \_ racine \_ paramètre \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ \_ exemple statique \_ desc \* \_ pStaticSamplers = null, D3D12 indicateurs de \_ \_ signature racine \_ indicateurs = D3D12 \_ \_ indicateur signature \_ racine \_ aucun)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description de \_ signature racine CD3DX12 \_ , en initialisant les paramètres suivants :

UINT numParameters

[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

possibilité UINT numStaticSamplers = 0

possibilité [**D3D12 \_ \_Exemple statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

possibilité [**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun

</dd> <dt>

**\_ \_ Description de la signature racine CD3DX12 \_ ( \_ valeur par défaut CD3DX12)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description de \_ signature racine CD3DX12 \_ , initialisée avec les paramètres par défaut.

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

**Inline init (UINT numParameters, const D3D12 \_ racine \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ un \_ échantillonneur statique \_ desc \* \_ pStaticSamplers = null, \_ D3D12 \_ indicateurs de signature racine \_ indicateurs = D3D12 \_ indicateur de \_ signature racine \_ \_ aucun)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT numParameters

[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

possibilité UINT numStaticSamplers = 0

possibilité [**D3D12 \_ \_Exemple statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

possibilité [**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun

</dd> <dt>

**static Inline init (D3D12 \_ racine de \_ SIGNATURE \_ desc &DESC, uint numParameters, const D3D12 \_ racine \_ \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ échantillon statique \_ \_ desc \* \_ pStaticSamplers = null, D3D12 indicateurs de \_ signature racine \_ \_ indicateurs = D3D12 \_ indicateur de signature racine \_ \_ \_ aucun)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ Description de la \_ signature racine \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &DESC

UINT numParameters

[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

possibilité UINT numStaticSamplers = 0

possibilité [**D3D12 \_ \_Exemple statique \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = null

possibilité [**D3D12 \_ Indicateurs \_ de \_ signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) indicateurs = \_ indicateur de signature racine D3D12 \_ \_ \_ aucun

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Description de la \_ signature racine D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





