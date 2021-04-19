---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une disposition d’entrée sous la forme d’un objet unique approprié pour une description de flux de données.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535795"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a>\_Structure de \_ \_ \_ disposition d’entrée de flux d’état de pipeline CD3DX12 \_

Structure d’assistance utilisée pour décrire une disposition d’entrée sous la forme d’un objet unique approprié pour une description de flux de données.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ \_ \_ Disposition d’entrée de flux d’état de pipeline CD3DX12 \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ \_ \_ \_ disposition d’entrée de flux d’état de pipeline CD3DX12 \_ .

</dd> <dt>

**\_ \_ \_ \_ Disposition d’entrée de flux d’état de pipeline CD3DX12 \_ ( \_ disposition d’entrée D3D12 \_ \_ desc const &i)**
</dt> <dd>

Crée une nouvelle instance d’une \_ disposition d’entrée de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ , initialisée avec un type de sous-objet de type de sous-objet de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_ \_** -objet copiées à partir de *i*, une structure de [**\_ \_ disposition \_ d’entrée de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .

</dd> <dt>

**Operator = (D3D12 \_ d’entrée \_ disposition \_ DESC const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**D3D12 \_ d’entrée \_ de l’opérateur \_ desc () const**
</dt> <dd>

Conversion implicite en une structure [**\_ \_ \_ desc d’entrée D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ \_ \_ La disposition d’entrée de flux d’état de pipeline CD3DX12 \_ est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ État de pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est définie comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
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

 

