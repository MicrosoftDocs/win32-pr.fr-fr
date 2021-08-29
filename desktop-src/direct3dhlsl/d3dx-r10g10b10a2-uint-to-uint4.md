---
title: D3DX_R10G10B10A2_UINT_to_UINT4 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur dxgi R10G10B10A2 uint dans un XMINT4.
ms.assetid: 47c4f11f-936a-46d5-9533-1a4f9fce6168
keywords:
- D3DX_R10G10B10A2_UINT_to_UINT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5470e206bdd28cb282bbe384efa095bec80bc52a5a9483c1f5c0a00611f5bb02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855479"
---
# <a name="d3dx_r10g10b10a2_uint_to_uint4-function"></a>D3DX \_ R10G10B10A2 \_ uint \_ à la \_ fonction UINT4

Décompresse les \_ \_ \_ données de nuanceur dxgi R10G10B10A2 uint dans un XMINT4.

## <a name="syntax"></a>Syntaxe

``` syntax
XMINT4 D3DX_R10G10B10A2_UINT_to_UINT4(
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

 

 





