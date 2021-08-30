---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_GS (D3dx12. h)
description: Structure d’assistance utilisée pour décrire un nuanceur Geometry en tant qu’objet unique approprié pour une description de flux.
ms.assetid: EAE81688-DAEE-4F7C-A80D-E33B364B2E8C
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_GS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_GS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2e2c891e303bf6e10c79ec06a71ef18a11b2df6e85d9f509f306f7515f4bf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119699"
---
# <a name="cd3dx12_pipeline_state_stream_gs-structure"></a>\_Structure de \_ \_ flux \_ GS d’État du pipeline CD3DX12

Structure d’assistance utilisée pour décrire un nuanceur Geometry en tant qu’objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_GS {
                                   CD3DX12_PIPELINE_STATE_STREAM_GS;
                                   CD3DX12_PIPELINE_STATE_STREAM_GS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_GS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Flux d’état de pipeline CD3DX12 \_ \_ \_ GS**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ GS.

</dd> <dt>

**CD3DX12 \_ pipeline \_ State \_ Stream \_ GS (D3D12 \_ SHADER \_ bytecode const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ GS, initialisé avec un type de sous-objet de type de sous-objet d' **État de \_ pipeline D3D12 \_ \_ \_ \_ GS** et des données de sous-objet copiées à partir de *i*, une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**Operator = (D3D12 \_ Shader \_ bytecode const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**Operator D3D12 \_ Shader \_ bytecode () const**
</dt> <dd>

Conversion implicite en une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> </dl>

## <a name="remarks"></a>Remarques

CD3DX12 \_ pipeline \_ \_ Stream état \_ GS est une spécialisation typedef du modèle de sous-objet de [**flux d' \_ État de pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_GS>
    CD3DX12_PIPELINE_STATE_STREAM_GS;
          
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

 

