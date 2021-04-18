---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY (D3dx12. h)
description: Structure d’assistance utilisée pour décrire la topologie primitive comme un objet unique approprié pour une description de flux.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529248"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a>\_Structure de \_ la \_ \_ topologie primitive du flux d’État du pipeline CD3DX12 \_

Structure d’assistance utilisée pour décrire la topologie primitive comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ \_ Topologie primitive du flux d’état \_ du pipeline CD3DX12 \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ topologie primitive de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_Topologie primitive du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ ( \_ type de topologie D3D12 primitif \_ \_ const &i)**
</dt> <dd>

Crée une nouvelle instance d’une \_ topologie primitive de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ , initialisée avec un type de sous-objet de type de sous-objet de sous-objet d'  **État de \_ pipeline \_ \_ \_ \_ \_ D3D12** et des données de sous-objet copiées à partir de i, une structure de [**\_ \_ \_ type de topologie primitive D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .

</dd> <dt>

**opérateur = (D3D12 \_ \_ type de topologie primitif \_ const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**D3D12 \_ , opérateur \_ \_ type de topologie primitif () const**
</dt> <dd>

Conversion implicite en une structure de [**\_ \_ \_ type de topologie primitive D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ \_ \_ La topologie primitive du flux d’État du pipeline CD3DX12 \_ est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est définie comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
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

 

