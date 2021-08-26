---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_HS (D3dx12. h)
description: Structure d’assistance utilisée pour décrire un nuanceur de coque comme un objet unique approprié pour une description de flux.
ms.assetid: 4958161D-3E79-4227-ADD7-7F53E34B2175
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_HS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_HS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b13c32c9da13a3cfce03605494bc8608a233f5979cb7b2757f203571c7901
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028359"
---
# <a name="cd3dx12_pipeline_state_stream_hs-structure"></a>\_ \_ \_ Structure HS du flux d’État du pipeline CD3DX12 \_

Structure d’assistance utilisée pour décrire un nuanceur de coque comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_HS {
                                   CD3DX12_PIPELINE_STATE_STREAM_HS;
                                   CD3DX12_PIPELINE_STATE_STREAM_HS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_HS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 de \_ flux d’État du pipeline \_ \_ \_ HS**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ HS.

</dd> <dt>

**CD3DX12 \_ pipeline \_ \_ Stream State \_ HS (D3D12 \_ SHADER \_ bytecode const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ HS, initialisé avec un type de sous-objet de type de sous-objet d' **État de \_ pipeline D3D12 \_ \_ \_ \_ HS** et des données de sous-objet copiées à partir de *i*, une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

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

CD3DX12 \_ pipeline \_ \_ Stream State \_ HS est une spécialisation typedef du modèle de sous-objet de [**flux d' \_ État de pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_HS>
    CD3DX12_PIPELINE_STATE_STREAM_HS;
          
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

 

