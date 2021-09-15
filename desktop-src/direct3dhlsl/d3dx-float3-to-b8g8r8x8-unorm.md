---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM fonction)
description: Compresse le XMFLOAT3 donné dans un \_ format dxgi \_ B8G8R8X8 \_ UNORM uint.
ms.assetid: 9492578b-e3c3-4856-b6d2-49f776a21d77
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d922264c62526b79aec5d3e36bb477e6a62987
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524833"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm-function"></a>D3DX \_ FLOAT3 \_ vers \_ B8G8R8X8 \_ UNORM, fonction

Compresse le XMFLOAT3 donné dans un \_ format dxgi \_ B8G8R8X8 \_ UNORM uint.

## <a name="syntax"></a>Syntaxe

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Données de nuanceur décompressées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

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

 

 





