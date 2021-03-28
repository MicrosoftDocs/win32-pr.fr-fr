---
title: D3DX_FLOAT_to_UINT fonction)
description: Convertit une valeur FLOAT en UINT.
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- D3DX_FLOAT_to_UINT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e729ba805d63068844192a134236722288fe8a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322694"
---
# <a name="d3dx_float_to_uint-function"></a>D3DX \_ float \_ to \_ uint, fonction

Convertit une valeur FLOAT en UINT.

## <a name="syntax"></a>Syntaxe

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*\_V* 
</dt> <dd>

Vecteur v.

</dd> <dt>

*\_Échelle* 
</dt> <dd>

Valeur de mise à l’échelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur FLOAT convertie

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

 

 





