---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 fonction)
description: Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8X8 UNORM dans un XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 fonction)
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc5f638d827a7b6ebf3543b3cde212fd56b0ace41ffb69bf4b7f79b56c28dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793855"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a>\_B8G8R8X8 \_ de D3DX UNORM \_ sRVB à la \_ \_ fonction FLOAT3

Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8X8 UNORM dans un XMFLOAT3.

## <a name="syntax"></a>Syntaxe

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(
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

 

 





