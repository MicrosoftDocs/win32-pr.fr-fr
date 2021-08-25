---
title: D3DX_INT_to_FLOAT fonction)
description: Convertit une valeur INT en valeur FLOAT.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- D3DX_INT_to_FLOAT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d49320c2b7bfd53b2fa4e0303a7d2e9bf6c22427557ee3827aed31f5915d1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855489"
---
# <a name="d3dx_int_to_float-function"></a>D3DX \_ int \_ to \_ float, fonction

Convertit une valeur INT en valeur FLOAT.

## <a name="syntax"></a>Syntaxe

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
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

Valeur int convertie.

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

 

 





