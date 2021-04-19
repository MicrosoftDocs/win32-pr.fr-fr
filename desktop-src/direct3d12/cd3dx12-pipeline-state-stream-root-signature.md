---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE (D3dx12. h)
description: Structure d’assistance utilisée pour décrire la signature racine comme un objet unique approprié pour une description de flux.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545894"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a>Structure de la signature de la \_ racine du flux d’État du pipeline CD3DX12 \_ \_ \_ \_

Structure d’assistance utilisée pour décrire la signature racine comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ \_ Signature racine du flux d’état \_ du pipeline CD3DX12 \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ signature racine de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_Signature racine du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ (ID3D12RootSignature \* const &i)**
</dt> <dd>

Crée une nouvelle instance d’une \_ signature racine de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ , initialisée avec un type de sous-objet de type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_ \_** -objet copiées à partir de *i*, une structure [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .

</dd> <dt>

**opérateur = (ID3D12RootSignature \* const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**\*const, opérateur ID3D12RootSignature ()**
</dt> <dd>

Conversion implicite en pointeur de structure [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ \_ \_ La signature racine du flux d’État du pipeline CD3DX12 \_ est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est définie comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

