---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK (D3dx12. h)
description: Structure d’assistance utilisée pour décrire un masque de nœud comme un objet unique approprié pour une description de flux.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c364ecd20459d8c20bdd3d30b969cc3b9ae46d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522571"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a>\_Structure de \_ \_ masque de nœud de flux d’état de \_ pipeline CD3DX12 \_

Structure d’assistance utilisée pour décrire un masque de nœud comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Masque de \_ \_ nœud du flux d’État du pipeline CD3DX12 \_ \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ masque de nœud de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_Masque de nœud du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ (uint const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ masque de nœud de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ , initialisée avec un type de sous-objet de type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_ \_** -objet copiées à partir de *i*, un masque de nœud **uint** .

</dd> <dt>

**opérateur = (UINT const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**const, opérateur ()**
</dt> <dd>

Conversion implicite en masque de nœud **uint** .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ \_ \_ \_ Le masque de nœud de flux d’état de pipeline CD3DX12 est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
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

 

