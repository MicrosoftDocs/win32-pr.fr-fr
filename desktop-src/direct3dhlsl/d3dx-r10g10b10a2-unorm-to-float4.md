---
title: D3DX_R10G10B10A2_UNORM_to_FLOAT4 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur de format dxgi R10G10B10A2 UNORM dans un XMFLOAT4.
ms.assetid: 36efd611-1450-421a-a34f-fd874589de2a
keywords:
- D3DX_R10G10B10A2_UNORM_to_FLOAT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3814bb8ed3bdcc1795a6452e88047c00f5d84cc6dbbfb835f4e4d0390df6c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286619"
---
# <a name="d3dx_r10g10b10a2_unorm_to_float4-function"></a>D3DX \_ R10G10B10A2 \_ UNORM \_ to \_ float4, fonction

Décompresse les \_ \_ \_ données de nuanceur de format dxgi R10G10B10A2 UNORM dans un XMFLOAT4.

## <a name="syntax"></a>Syntaxe

``` syntax
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*packedInput* 
</dt> <dd>

Données de nuanceur compressées.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

 

 





