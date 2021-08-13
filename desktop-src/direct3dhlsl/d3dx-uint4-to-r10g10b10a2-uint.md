---
title: D3DX_UINT4_to_R10G10B10A2_UINT fonction)
description: Recompresse le XMINT4 donné dans un \_ format dxgi \_ R10G10B10A2 \_ uint.
ms.assetid: fe10c62e-2d84-4f6b-886b-247ee344f6c7
keywords:
- D3DX_UINT4_to_R10G10B10A2_UINT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R10G10B10A2_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33420ca720ce2e605a378340926f86651a39e6e7f4c787c83d5e4ba2b15a8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286474"
---
# <a name="d3dx_uint4_to_r10g10b10a2_uint-function"></a>D3DX \_ UINT4 \_ à \_ R10G10B10A2 \_ uint, fonction

Recompresse le XMINT4 donné dans un \_ format dxgi \_ R10G10B10A2 \_ uint.

## <a name="syntax"></a>Syntaxe

``` syntax
UINT D3DX_UINT4_to_R10G10B10A2_UINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Données du nuanceur à compresser.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Données de nuanceur compressées.

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

 

 





