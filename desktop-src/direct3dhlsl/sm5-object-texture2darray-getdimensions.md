---
title: 'Texture2DArray :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture2DArray :: GetDimensions,, fonction'
ms.assetid: 0f6d88b3-195d-4f8c-ac31-ac90129a233e
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
ms.openlocfilehash: c655313147a568e5eb33ddf30a2acd2be3549ca4d57bc8510ef974199ea3740d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985869"
---
# <a name="texture2darraygetdimensions-function"></a>Texture2DArray :: GetDimensions,, fonction

Retourne les dimensions de la ressource.

## <a name="syntax"></a>Syntaxe

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*MipLevel* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Facultatif. Le niveau de mipmap (doit être spécifié si *NumberOfLevels* est utilisé).

</dd> <dt>

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

*NumberOfLevels* \[ à\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre de niveaux de mipmap (requiert également *MipLevel* ).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Rien

## <a name="remarks"></a>Remarques

Il s’agit d’une liste des versions surchargées de cette méthode.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out float Height,
  out float Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
