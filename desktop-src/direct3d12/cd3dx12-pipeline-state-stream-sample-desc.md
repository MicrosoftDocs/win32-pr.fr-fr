---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC (D3dx12. h)
description: Structure d’assistance utilisée pour décrire une description d’exemple comme un objet unique approprié pour une description de flux.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538548"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a>\_Exemple de \_ \_ \_ \_ structure DESC de flux d’état de pipeline CD3DX12

Structure d’assistance utilisée pour décrire une description d’exemple comme un objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Exemple de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ desc**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ exemple de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ desc.

</dd> <dt>

**\_ \_ Exemple de flux d’état de pipeline CD3DX12 \_ \_ \_ desc ( \_ exemple dxgi \_ desc const &i)**
</dt> <dd>

Crée une nouvelle instance d’un \_ exemple de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ desc, initialisé avec un type de sous-objet de type de sous-objet d' **État de pipeline D3D12 et des données de \_ \_ \_ \_ sous \_ \_** -objet copiées à partir de *i*, une structure d' [**\_ exemple \_ desc de dxgi**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .

</dd> <dt>

**Operator = ( \_ exemple dxgi \_ desc const& i)**
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**exemple DXGI \_ \_ desc () const, opérateur**
</dt> <dd>

Conversion implicite en une structure d' [**\_ exemple \_ desc dxgi**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .

</dd> </dl>

## <a name="remarks"></a>Notes

\_ \_ \_ \_ L’exemple de flux d’état de pipeline CD3DX12 \_ desc est une spécialisation typedef du modèle de sous- [**objet de flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) , et est défini comme suit :


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
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

 

