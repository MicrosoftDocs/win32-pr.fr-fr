---
title: D3DX_B8G8R8X8_UNORM_to_FLOAT3 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur de format dxgi B8G8R8X8 UNORM dans un XMFLOAT3.
ms.assetid: 0987d71a-89a4-4751-9f32-08e2490204d2
keywords:
- D3DX_B8G8R8X8_UNORM_to_FLOAT3 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6397f271899c2a8d73ed1ba84a04f3c02514fb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232559"
---
# <a name="d3dx_b8g8r8x8_unorm_to_float3-function"></a>D3DX \_ B8G8R8X8 \_ UNORM \_ to \_ FLOAT3, fonction

Décompresse les \_ \_ \_ données de nuanceur de format dxgi B8G8R8X8 UNORM dans un XMFLOAT3.

## <a name="syntax"></a>Syntaxe

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*packedInput* 
</dt> <dd>

Données de nuanceur compressées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Données de nuanceur décompressées.

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

 

 





