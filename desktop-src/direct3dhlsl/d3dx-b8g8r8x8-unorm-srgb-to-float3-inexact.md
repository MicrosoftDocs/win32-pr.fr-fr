---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact fonction)
description: Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8X8 UNORM dans un XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact fonction)
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ef3f0b97ee3d5e21fef7b0227304fc5b187df2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974451"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a>D3DX \_ B8G8R8X8 \_ UNORM \_ sRVB \_ à \_ FLOAT3 \_ fonction inexacte

Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8X8 UNORM dans un XMFLOAT3.

## <a name="syntax"></a>Syntaxe

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
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

## <a name="remarks"></a>Notes

Cette fonction utilise des instructions de nuanceur qui n’ont pas une précision suffisamment élevée pour fournir la réponse exacte. La fonction alternative [**D3DX \_ B8G8R8X8 \_ UNORM \_ sRVB \_ à \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) utilise une table de recherche stockée dans le nuanceur pour fournir une conversion d’sRGB en float exacte.

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

 

 





