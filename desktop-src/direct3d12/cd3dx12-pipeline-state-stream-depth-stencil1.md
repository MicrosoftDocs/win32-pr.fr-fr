---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une description de stencil de profondeur comme un objet unique approprié pour une description de flux. | Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f04064a7ab4a7ca100e48da2446501d4415b693ce6abdf213f121952cc8f198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632526"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a>\_ \_ \_ \_ Structure STENCIL1 de profondeur du flux d’État du pipeline CD3DX12 \_

Structure d’assistance utilisée pour décrire une description de stencil de profondeur comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Profondeur du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ STENCIL1**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ STENCIL1 de profondeur du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**CD3DX12 \_ de la profondeur du flux d’État du pipeline \_ \_ \_ \_ STENCIL1 ( \_ stencil de profondeur CD3DX12 \_ \_ DESC1 const &i)**
</dt> <dd>

Crée une instance d’une profondeur de \_ flux d’état de pipeline CD3DX12 \_ \_ \_ \_ STENCIL1, initialisée avec un type de sous-objet de **D3D12 \_ profondeur de type de sous-objet d’état de pipeline \_ \_ \_ \_ \_ STENCIL1** et des données de sous-objet copiées à partir de *i*, une structure CD3DX12 de [**\_ stencil de profondeur \_ \_ DESC1**](cd3dx12-depth-stencil-desc1.md) .

</dd> <dt>

**Operator = (CD3DX12 de \_ profondeur du \_ stencil \_ DESC1 const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**CD3DX12 \_ de profondeur \_ de l’opérateur \_ DESC1 () const**
</dt> <dd>

Conversion implicite en [**structure \_ \_ \_ DESC1 du stencil de profondeur CD3DX12**](cd3dx12-depth-stencil-desc1.md) .

</dd> </dl>

## <a name="remarks"></a>Remarques

\_ \_ \_ \_ La profondeur du flux d’État du pipeline CD3DX12 \_ STENCIL1 est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) et est définie comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
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

 

