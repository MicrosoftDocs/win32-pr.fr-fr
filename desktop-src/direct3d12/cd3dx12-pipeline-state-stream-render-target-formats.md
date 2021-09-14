---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS (D3dx12. h)
description: Structure d’assistance utilisée pour décrire les formats de cible de rendu sous la forme d’un objet unique approprié pour une description de flux.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921503"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a>\_Structure de \_ \_ \_ \_ formats cibles de rendu du flux \_ d’État du pipeline CD3DX12

Structure d’assistance utilisée pour décrire les formats de cible de rendu sous la forme d’un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ \_ \_ Formats cibles de rendu du flux d' \_ état \_ du pipeline CD3DX12**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ Formats cibles de rendu du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ (D3D12 \_ RT \_ format \_ const &i)**
</dt> <dd>

Crée une nouvelle instance d’un flux de données d' \_ État de pipeline CD3DX12 \_ \_ \_ \_ \_ . les formats cibles sont initialisés avec un type de sous-objet de **type de sous-objet d’état de pipeline D3D12. les \_ \_ \_ \_ \_ \_ \_ formats cibles** et les données de sous-objet copiés à partir de *i*, une structure de [**\_ \_ \_ tableau de format D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> <dt>

**Operator = (D3D12 \_ RT \_ format \_ tableau const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**Operator D3D12 \_ RT \_ format \_ tableau () const**
</dt> <dd>

Conversion implicite en structure de [**\_ tableau de \_ format \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ \_ \_ \_ \_ Les formats de cible de rendu du flux d’État du pipeline CD3DX12 sont une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et sont définis comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
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

 

