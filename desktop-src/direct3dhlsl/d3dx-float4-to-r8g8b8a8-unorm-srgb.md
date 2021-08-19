---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB fonction)
description: Recompresse le XMFLOAT4 donné dans un \_ format dxgi \_ R8G8B8A8 \_ UNORM \_ sRVB.
ms.assetid: 66580428-6f06-4e0c-bf89-01f03c7304ad
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e930935e34ff1aa76c99949949e12b5c57254eeea59262cf2ec7828482965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516277"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm_srgb-function"></a>D3DX \_ float4 \_ to \_ R8G8B8A8 \_ UNORM \_ sRGB, fonction

Recompresse le XMFLOAT4 donné dans un \_ format dxgi \_ R8G8B8A8 \_ UNORM \_ sRVB.

## <a name="syntax"></a>Syntaxe

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Données du nuanceur à compresser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

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

 

 





