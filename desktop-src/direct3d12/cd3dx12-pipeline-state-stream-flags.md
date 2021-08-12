---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_FLAGS (D3dx12. h)
description: Structure d’assistance utilisée pour décrire les indicateurs d’état de pipeline sous la forme d’un objet unique approprié pour une description de flux.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_FLAGS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8789fb8c393ecaf83e0295654092b22aba7f497abf909c46bac422d442c6fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530708"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a>\_Structure d' \_ \_ indicateurs du flux d’État du pipeline CD3DX12 \_

Structure d’assistance utilisée pour décrire les indicateurs d’état de pipeline sous la forme d’un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Indicateurs du \_ flux d’État du PIPELINe CD3DX12 \_ \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ indicateur de flux d’état de pipeline CD3DX12 \_ \_ \_ .

</dd> <dt>

**Indicateurs de flux d’État du pipeline CD3DX12 \_ \_ \_ \_ ( \_ indicateurs d’état de pipeline D3D12 \_ \_ const &i)**
</dt> <dd>

Crée une nouvelle instance d’indicateurs de \_ flux d’état de pipeline CD3DX12 \_ \_ \_ , initialisée avec un type de sous-objet des indicateurs de type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_** -objet copiées à partir de *i*, une structure d' [**indicateurs d' \_ \_ état \_ de pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .

</dd> <dt>

**Operator = (D3D12 \_ pipeline \_ State \_ flags const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**D3D12 \_ , opérateur \_ indicateurs d’état de pipeline \_ () const**
</dt> <dd>

Conversion implicite en une structure d' [**\_ indicateurs d' \_ état \_ de pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .

</dd> </dl>

## <a name="remarks"></a>Remarques

\_ \_ \_ \_ Les indicateurs de flux d’état de pipeline CD3DX12 sont une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et sont définis comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
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

 

