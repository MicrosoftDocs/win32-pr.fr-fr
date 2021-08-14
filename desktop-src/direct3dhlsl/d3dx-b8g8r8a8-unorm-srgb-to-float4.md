---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 fonction)
description: Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8A8 UNORM dans un XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 fonction)
ms.assetid: f6ce6125-c67e-4545-b25e-3400c0fc62b1
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620823a572b7eb23f05bdda83866aae982f326dfb70ca6856309abc9d96f05b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516595"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4-function"></a>\_B8G8R8A8 \_ de D3DX UNORM \_ sRVB à la \_ \_ fonction float4

Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8A8 UNORM dans un XMFLOAT4.

## <a name="syntax"></a>Syntaxe

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(
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

 

 





