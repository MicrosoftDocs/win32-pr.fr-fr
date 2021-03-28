---
title: D3DX_R8G8B8A8_SNORM_to_FLOAT4 fonction)
description: Décompresse le \_ format dxgi \_ R8G8B8A8 \_ ronfler les données de nuanceur dans un XMFLOAT4.
ms.assetid: 2f2b9d5e-f4d0-470a-a4bb-b333d57f03e7
keywords:
- D3DX_R8G8B8A8_SNORM_to_FLOAT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a4153fa30f2792008ccc45bc3e16f5d404f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974522"
---
# <a name="d3dx_r8g8b8a8_snorm_to_float4-function"></a>D3DX \_ R8G8B8A8 \_ ronfler \_ à la \_ fonction float4

Décompresse le \_ format dxgi \_ R8G8B8A8 \_ ronfler les données de nuanceur dans un XMFLOAT4.

## <a name="syntax"></a>Syntaxe

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(
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

 

 





