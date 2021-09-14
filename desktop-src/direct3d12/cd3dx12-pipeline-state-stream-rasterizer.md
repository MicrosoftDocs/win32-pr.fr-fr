---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une description de rastériseur comme un objet unique approprié pour une description de flux.
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921504"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a>\_Structure de \_ \_ rastériseur du flux d’État du pipeline CD3DX12 \_

Structure d’assistance utilisée pour décrire une description de rastériseur comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Rastériseur de \_ flux d’état de PIPELINe CD3DX12 \_ \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ rastériseur de flux d’état de pipeline CD3DX12 \_ \_ \_ .

</dd> <dt>

**\_ \_ Rastériseur de flux d’état de pipeline CD3DX12 \_ \_ (CD3DX12 \_ rastériseur \_ desc const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ rastériseur de flux d’état de pipeline CD3DX12 \_ \_ \_ , initialisée avec un type de sous-objet de type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_** -objet copiées à partir de *i*, une structure de [**\_ rastériseur CD3DX12 \_ desc**](cd3dx12-rasterizer-desc.md) .

</dd> <dt>

**Operator = (CD3DX12 \_ rastériseur \_ desc const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**opérateur CD3DX12 \_ rastériseur \_ desc () const**
</dt> <dd>

Conversion implicite en une structure [**CD3DX12 \_ rastériseur \_ desc**](cd3dx12-rasterizer-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ \_ \_ Le rastériseur de flux d’état de pipeline CD3DX12 est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
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

 

