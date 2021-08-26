---
title: D3DX_R16G16_SNORM_to_FLOAT2 fonction)
description: Décompresse le \_ format dxgi \_ R16G16 \_ ronfler les données de nuanceur dans un XMFLOAT2.
ms.assetid: b54df555-b71f-46cd-8be7-34de785d15e2
keywords:
- D3DX_R16G16_SNORM_to_FLOAT2 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589954208886b7dccf4f48d2724c98ab4404d5394b73d894a8eb4924e152cdcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983239"
---
# <a name="d3dx_r16g16_snorm_to_float2-function"></a>D3DX \_ R16G16 \_ ronfler \_ à la \_ fonction FLOAT2

Décompresse le \_ format dxgi \_ R16G16 \_ ronfler les données de nuanceur dans un XMFLOAT2.

## <a name="syntax"></a>Syntaxe

``` syntax
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(
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

 

 





