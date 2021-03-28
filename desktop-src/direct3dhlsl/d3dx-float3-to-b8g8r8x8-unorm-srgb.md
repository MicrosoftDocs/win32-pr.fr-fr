---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB fonction)
description: Recompresse le XMFLOAT3 donné dans un \_ format dxgi \_ B8G8R8X8 \_ UNORM \_ sRVB.
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74dd5fbc1329d884968d76039061fceb22aafbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992176"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a>D3DX \_ FLOAT3 \_ to \_ B8G8R8X8 \_ UNORM \_ sRGB, fonction

Recompresse le XMFLOAT3 donné dans un \_ format dxgi \_ B8G8R8X8 \_ UNORM \_ sRVB.

## <a name="syntax"></a>Syntaxe

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions](format-conversion-functions.md)
</dt> <dt>

[Décompresser et compresser le \_ format DXGI pour la modification des images In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





