---
title: D3DX_SRGB_to_FLOAT_inexact fonction)
description: Convertit une valeur sRVB en valeur FLOAT. | D3DX_SRGB_to_FLOAT_inexact fonction)
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9dd841e022da85d609c203f57288af62a6c99ecc9f56079982308a095285f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515690"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>D3DX \_ sRVB \_ en \_ float, \_ fonction inexacte

Convertit une valeur sRVB en valeur FLOAT.

## <a name="syntax"></a>Syntaxe

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*multiples* 
</dt> <dd>

Valeur sRVB à convertir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur sRVB convertie.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas une précision suffisamment élevée pour fournir la réponse exacte. La fonction alternative de [**D3DX \_ sRVB \_ en \_ float**](d3dx-srgb-to-float.md) utilise une table de recherche pour fournir une conversion d’sRVB en valeurs flottantes exacte.

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

 

 





