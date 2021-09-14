---
title: 'Texture2DMS :: GetSamplePosition, fonction'
description: Retourne la position d’échantillon pour l’exemple d’index fourni.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
keywords:
- GetSamplePosition fonction HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922300"
---
# <a name="texture2dmsgetsampleposition-function"></a>Texture2DMS :: GetSamplePosition, fonction

Retourne la position d’échantillon pour l’exemple d’index fourni.

## <a name="syntax"></a>Syntaxe

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*sampleindex* \[ dans\]
</dt> <dd>

Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Index de base zéro d’un emplacement d’échantillon.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **float2**

Exemple d’emplacement.

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
