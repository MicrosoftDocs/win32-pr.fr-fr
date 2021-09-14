---
title: 'Texture2D :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture2D :: GetDimensions,, fonction'
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921231"
---
# <a name="texture2dgetdimensions-function"></a>Texture2D :: GetDimensions,, fonction

Retourne les dimensions de la ressource.

## <a name="syntax"></a>Syntaxe

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*MipLevel* \[ dans\]
</dt> <dd>

Type : **uint**

facultatif. Le niveau de mipmap (doit être spécifié si *NumberOfLevels* est utilisé).

</dd> <dt>

*Largeur* \[ à\]
</dt> <dd>

Type : **uint**

Largeur des ressources, en texels.

</dd> <dt>

*Hauteur* \[ à\]
</dt> <dd>

Type : **uint**

Hauteur des ressources, en texels.

</dd> <dt>

*NumberOfLevels* \[ à\]
</dt> <dd>

Type : **uint**

Nombre de niveaux de mipmap (requiert également *MipLevel* ).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Rien

## <a name="remarks"></a>Notes

Il s’agit d’une liste des versions surchargées de cette méthode.


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




