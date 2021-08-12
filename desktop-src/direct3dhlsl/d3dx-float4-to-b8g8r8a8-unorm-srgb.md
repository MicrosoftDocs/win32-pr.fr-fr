---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB fonction)
description: Compresse le XMFLOAT4 donné dans un \_ format dxgi \_ B8G8R8A8 \_ UNORM \_ sRVB uint.
ms.assetid: 2fc36f19-44ce-43ba-9d9f-e8061f94a207
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6661ea7bce5f5a10fec8c3d96bf178fc4e169ba53d013143b89c8114de71cc60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286835"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm_srgb-function"></a>D3DX \_ float4 \_ to \_ B8G8R8A8 \_ UNORM \_ sRGB, fonction

Compresse le XMFLOAT4 donné dans un \_ format dxgi \_ B8G8R8A8 \_ UNORM \_ sRVB uint.

## <a name="syntax"></a>Syntaxe

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Données de nuanceur décompressées.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Données de nuanceur compressées.

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

 

 





