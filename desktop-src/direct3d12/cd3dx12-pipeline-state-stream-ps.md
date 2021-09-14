---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_PS (D3dx12. h)
description: Structure d’assistance utilisée pour décrire un nuanceur de pixels comme un objet unique approprié pour une description de flux.
ms.assetid: A71E2ABE-5B52-41B4-ACE0-25CA63EF2565
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_PS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f3b49328ad85bc68147ad58b043459c223e6a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921507"
---
# <a name="cd3dx12_pipeline_state_stream_ps-structure"></a>\_Structure de flux d’état de pipeline CD3DX12 \_ \_ \_ PS

Structure d’assistance utilisée pour décrire un nuanceur de pixels comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PS {
                                   CD3DX12_PIPELINE_STATE_STREAM_PS;
                                   CD3DX12_PIPELINE_STATE_STREAM_PS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Flux d’État du pipeline CD3DX12 \_ \_ \_ PS**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ PS.

</dd> <dt>

**\_Flux d’État du pipeline CD3DX12 \_ \_ \_ PS (D3D12 \_ Shader- \_ bytecode const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ PS, initialisé avec un type de sous-objet de type de sous-objet d' **État de \_ pipeline D3D12 \_ \_ \_ \_ PS** et des données de sous-objet copiées à partir de *i*, une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**Operator = (D3D12 \_ Shader \_ bytecode const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**Operator D3D12 \_ Shader \_ bytecode () const**
</dt> <dd>

Conversion implicite en une structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ \_ Le flux d’état de pipeline CD3DX12 \_ PS est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PS>
    CD3DX12_PIPELINE_STATE_STREAM_PS;
          
```



## <a name="requirements"></a>Spécifications



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

 

