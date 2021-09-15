---
title: 'RWTexture2DArray :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | RWTexture2DArray :: GetDimensions,, fonction'
ms.assetid: 473b3f41-854d-4881-a80b-2d2dd7e5d479
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
ms.openlocfilehash: 6d95148cb6dc51c739ee4546bd64ce22666d5fd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413225"
---
# <a name="rwtexture2darraygetdimensions-function"></a>RWTexture2DArray :: GetDimensions,, fonction

Retourne les dimensions de la ressource.

## <a name="syntax"></a>Syntaxe

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements
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

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Il s’agit d’une liste des versions surchargées de cette méthode.


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Elements);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWTexture2DArray](sm5-object-rwtexture2darray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
