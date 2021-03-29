---
title: D3DX_FLOAT2_to_R16G16_UNORM fonction)
description: Recompresse le XMFLOAT2 donné dans un \_ UNORM de format dxgi \_ R16G16 \_ .
ms.assetid: 5a1bd034-262f-4f55-8f38-d2fda42bb13b
keywords:
- D3DX_FLOAT2_to_R16G16_UNORM fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0a6ffe3081955db79765d80278394eb89ab188
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992209"
---
# <a name="d3dx_float2_to_r16g16_unorm-function"></a>D3DX \_ FLOAT2 \_ vers \_ R16G16 \_ UNORM, fonction

Recompresse le XMFLOAT2 donné dans un \_ UNORM de format dxgi \_ R16G16 \_ .

## <a name="syntax"></a>Syntaxe

``` syntax
UINT D3DX_FLOAT2_to_R16G16_UNORM(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Données de nuanceur décompressées.

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

 

 





