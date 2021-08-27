---
title: D3DX_B8G8R8A8_UNORM_to_FLOAT4 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur de format dxgi B8G8R8A8 UNORM dans un XMFLOAT4.
ms.assetid: 1a52058c-825d-4607-b67d-8226dccdee54
keywords:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f82f827342cffbf34bde649a3e9a50f2fb42e7ef06b8bdd43a639298e6b0a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025049"
---
# <a name="d3dx_b8g8r8a8_unorm_to_float4-function"></a>D3DX \_ B8G8R8A8 \_ UNORM \_ to \_ float4, fonction

Décompresse les \_ \_ \_ données de nuanceur de format dxgi B8G8R8A8 UNORM dans un XMFLOAT4.

## <a name="syntax"></a>Syntaxe

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(
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

 

 





