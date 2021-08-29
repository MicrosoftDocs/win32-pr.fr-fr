---
title: D3DX_R16G16_FLOAT_to_FLOAT2 fonction)
description: Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8X8 UNORM dans un XMFLOAT2.
ms.assetid: 6c57dc86-d034-4b54-8572-44ac3738beb9
keywords:
- D3DX_R16G16_FLOAT_to_FLOAT2 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_FLOAT_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8bb60ed211fa919c511a2061871ae47cd5eacaa29d37df7442939d0eedfb70a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855469"
---
# <a name="d3dx_r16g16_float_to_float2-function"></a>D3DX \_ R16G16 \_ float \_ to \_ FLOAT2, fonction

Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8X8 UNORM dans un XMFLOAT2.

## <a name="syntax"></a>Syntaxe

``` syntax
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*packedInput* 
</dt> <dd>

Données de nuanceur compressées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Données de nuanceur décompressées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions](format-conversion-functions.md)
</dt> <dt>

[Décompresser et compresser le \_ format DXGI pour la modification des images In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





