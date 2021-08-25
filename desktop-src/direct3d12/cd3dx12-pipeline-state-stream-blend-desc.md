---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une description de Blend comme un objet unique approprié pour une description de flux.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300506d2c41be5a5380f4f0f64c93779185fd59ced2e0dd613d926f8397ea85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752169"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a>\_Structure de \_ \_ \_ mélange DESC du flux d’État du pipeline CD3DX12 \_

Structure d’assistance utilisée pour décrire une description de Blend comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ \_ \_ Mélange DESC du flux d’État du pipeline CD3DX12 \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ \_ desc.

</dd> <dt>

**\_Flux d' \_ État de pipeline CD3DX12 \_ \_ \_ desc (CD3DX12 \_ Blend \_ desc const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ Blend \_ , initialisé avec un type de sous-objet de **type de sous-objet d’état de \_ pipeline D3D12 \_ \_ \_ \_ Blend** et des données de sous-objet copiées à partir de *i*, une structure [**CD3DX12 \_ Blend \_ desc**](cd3dx12-blend-desc.md) .

</dd> <dt>

**opérateur = (CD3DX12 \_ Blend \_ desc const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**opérateur CD3DX12 \_ Blend \_ desc () const**
</dt> <dd>

Conversion implicite en une structure [**CD3DX12 \_ Blend \_ desc**](cd3dx12-blend-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Remarques

CD3DX12 \_ pipeline \_ \_ Stream State \_ Blend \_ est une spécialisation typedef du modèle de sous-objet de [**\_ flux d' \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
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

 

