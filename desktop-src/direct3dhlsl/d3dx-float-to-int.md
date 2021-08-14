---
title: D3DX_FLOAT_to_INT fonction)
description: Convertit une valeur FLOAT en INT.
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- D3DX_FLOAT_to_INT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb76c5c459daaaba4dd7d038b65b9dc34e895f283b66545684ef1f5fb10c95cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516662"
---
# <a name="d3dx_float_to_int-function"></a>\_Fonction D3DX float \_ to \_ int

Convertit une valeur FLOAT en INT.

## <a name="syntax"></a>Syntaxe

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*\_V* 
</dt> <dd>

Valeur v.

</dd> <dt>

*\_Scale* 
</dt> <dd>

Valeur de mise à l’échelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur FLOAT convertie

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

 

 





