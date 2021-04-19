---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO (D3dx12. h)
description: Structure d’assistance utilisée pour décrire un PSO mis en cache comme un objet unique approprié pour une description de flux.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539427"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>CD3DX12 \_ - \_ \_ structure d' \_ PSO mise en cache de flux d’état de pipeline \_

Structure d’assistance utilisée pour décrire un PSO mis en cache comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Flux d' \_ État du pipeline CD3DX12 \_ \_ mis en cache \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ mis en cache pour un objet \_ PSO.

</dd> <dt>

**\_Flux d' \_ État de pipeline CD3DX12 \_ \_ PSO mis en cache \_ (D3D12 d' \_ État de pipeline mis en cache \_ \_ const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ mis en cache \_ PSO, initialisé avec un type de sous-objet de **type de sous-objet d’état de \_ pipeline D3D12 \_ \_ \_ \_ mis en cache \_ PSO** et des données de sous-objet copiées à partir de *i*, une structure d' [**\_ \_ \_ État de pipeline mise en cache D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .

</dd> <dt>

**Operator = (D3D12 d' \_ État du pipeline mis en cache \_ \_ const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**D3D12 \_ \_ de pipeline \_ () const d’opérateur () const**
</dt> <dd>

Conversion implicite en structure d' [**\_ \_ \_ État de pipeline mise en cache D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ Flux d’état de pipeline CD3DX12 \_ \_ , PSO mis en cache \_ est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ État de pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
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

 

