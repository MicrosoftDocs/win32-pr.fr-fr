---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une description de stencil de profondeur comme un objet unique approprié pour une description de flux. | Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921548"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a>\_Structure du \_ \_ stencil de profondeur du flux d’État du \_ pipeline CD3DX12 \_

Structure d’assistance utilisée pour décrire une description de stencil de profondeur comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Stencil de \_ \_ profondeur du flux d’État du pipeline CD3DX12 \_ \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ stencil de profondeur de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**CD3DX12 \_ \_ stencil de profondeur du flux d’État du pipeline \_ \_ \_ (CD3DX12 \_ \_ \_ desc const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ stencil de profondeur de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ , initialisée avec un type de sous-objet du **stencil de profondeur de D3D12 d’État du \_ pipeline et des données de \_ \_ \_ sous \_ \_** -objet copiées à partir de *i*, une structure [**\_ \_ \_ desc du stencil de profondeur CD3DX12**](cd3dx12-depth-stencil-desc.md) .

</dd> <dt>

**Operator = (CD3DX12 de \_ profondeur du \_ stencil \_ const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**CD3DX12 \_ \_ \_ () const du stencil de profondeur de l’opérateur**
</dt> <dd>

Conversion implicite en [**structure \_ \_ \_ desc du stencil de profondeur CD3DX12**](cd3dx12-depth-stencil-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ \_ \_ \_ Le stencil de profondeur du flux d’État du pipeline CD3DX12 est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
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

 

