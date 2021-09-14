---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT (D3dx12. h)
description: Structure d’assistance utilisée pour décrire le format de stencil de profondeur comme un objet unique approprié pour une description de flux.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921551"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a>\_Structure du \_ \_ format du \_ stencil de profondeur du flux d' \_ État du pipeline CD3DX12 \_

Structure d’assistance utilisée pour décrire le format de stencil de profondeur comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Format du \_ \_ stencil de profondeur du flux d’État du \_ \_ pipeline CD3DX12 \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ format de stencil de profondeur de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ Format de stencil de profondeur du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ ( \_ format dxgi const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ format de stencil de profondeur de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ \_ , initialisée avec un type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_ \_ \_** -objet copiées à partir de *i*, une énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

</dd> <dt>

**opérateur = (DXGI \_ format const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**\_const, opérateur de format dxgi ()**
</dt> <dd>

Conversion implicite en une énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ \_ \_ \_ \_ Le format de stencil de profondeur du flux d’État du pipeline CD3DX12 est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
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

 

