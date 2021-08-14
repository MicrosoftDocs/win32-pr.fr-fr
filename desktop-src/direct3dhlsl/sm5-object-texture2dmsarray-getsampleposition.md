---
title: 'Texture2DMSArray :: GetSamplePosition, fonction'
description: 'Obtient la position de l’échantillon spécifié. | Texture2DMSArray :: GetSamplePosition, fonction'
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
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
ms.openlocfilehash: 9da6727120dcb19d9dd51c83d62f85d842036edb2197d33e298259480b248642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508415"
---
# <a name="texture2dmsarraygetsampleposition-function"></a>Texture2DMSArray :: GetSamplePosition, fonction

Obtient la position de l’échantillon spécifié.

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

## <a name="return-value"></a>Valeur retournée

Type : **float2**

Exemple d’emplacement.

## <a name="remarks"></a>Remarques

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
