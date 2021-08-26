---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE (D3dx12. h)
description: Structure d’assistance utilisée pour décrire la valeur de coupe de la bande de mémoire tampon d’index comme un objet unique approprié pour une description de flux.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e204b4f89cced7cf0bd5cdcb21702c37c241a81abfbc12d8644eafdb3c7c7ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988409"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a>\_Flux d’État du pipeline CD3DX12-structure de \_ \_ \_ \_ \_ valeur de coupe \_

Structure d’assistance utilisée pour décrire la valeur de coupe de la bande de mémoire tampon d’index comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 de \_ flux d’état de pipeline \_ IB- \_ \_ \_ \_ valeur de coupe \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ flux d’état de pipeline CD3DX12 valeur de coupe de la \_ \_ \_ \_ barrette IB \_ \_ .

</dd> <dt>

**\_Flux d’État du pipeline CD3DX12- \_ \_ \_ \_ \_ valeur de coupe de bande IB \_ (valeur de coupe de la \_ bande tampon d’index D3D12 \_ \_ \_ \_ const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ flux d’état de pipeline CD3DX12 \_ \_ \_ \_ \_ \_ , initialisée avec un type de sous-objet **d' \_ État de pipeline D3D12, \_ type de \_ \_ sous \_ \_ \_ \_** -objet de sous-objet IB de la valeur de coupe et des données de sous-objet copiées à partir de *i*, une structure de valeur de coupe de la [**\_ \_ bande de mémoire tampon \_ \_ \_ d’index D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .

</dd> <dt>

**Operator = (valeur de coupe de la \_ bande tampon d’index D3D12 \_ \_ \_ \_ const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**\_ \_ valeur de coupe de la bande de la mémoire tampon d’index D3D12 \_ \_ \_ () const**
</dt> <dd>

Conversion implicite en une structure de [**\_ \_ \_ \_ \_ valeur de coupe de mémoire tampon d’index D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .

</dd> </dl>

## <a name="remarks"></a>Remarques

\_Flux d’État du pipeline CD3DX12 \_ \_ \_ \_ \_ \_ la valeur de coupe de la bande IB est une spécialisation typedef du modèle de sous-objet de flux d' [**\_ État du pipeline \_ \_ \_ CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est définie comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
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

 

