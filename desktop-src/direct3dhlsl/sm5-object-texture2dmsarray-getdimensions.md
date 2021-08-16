---
title: 'Texture2DMSArray :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture2DMSArray :: GetDimensions,, fonction'
ms.assetid: 86d54e0d-f168-479f-b2af-f021b8994741
keywords:
- GetDimensions, fonction HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d6f9d4fc24cb1f8933bdb67796aebe3fe7d7406b114eea8a12f507c5f04591f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508425"
---
# <a name="texture2dmsarraygetdimensions-function"></a>Texture2DMSArray :: GetDimensions,, fonction

Retourne les dimensions de la ressource.

## <a name="syntax"></a>Syntaxe

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Largeur* \[ à\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Largeur des ressources, en texels.

</dd> <dt>

*Hauteur* \[ à\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Hauteur des ressources, en texels.

</dd> <dt>

*Éléments* \[ à\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’éléments dans le tableau.

</dd> <dt>

*NumberOfSamples* \[ à\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’emplacements d’échantillonnage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Rien

## <a name="remarks"></a>Remarques

Il s’agit d’une liste des versions surchargées de cette méthode.


```
void GetDimensions(out float Width,
  out float Height,
  out float Elements,
  out float NumberOfSamples);
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
