---
title: 'Texture1D :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture1D :: GetDimensions,, fonction'
ms.assetid: eb8fc02f-01c8-44b9-9d7e-faf59660c287
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
ms.openlocfilehash: fdd9b79a1cc1fa2a5a8db3e0db7a7163878b066b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530706"
---
# <a name="texture1dgetdimensions-function"></a>Texture1D :: GetDimensions,, fonction

Retourne les dimensions de la ressource.

## <a name="syntax"></a>Syntaxe

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*MipLevel* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

facultatif. Le niveau de mipmap (doit être spécifié si *NumberOfLevels* est utilisé).

</dd> <dt>

*Largeur* \[ à\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Largeur des ressources, en texels.

</dd> <dt>

*NumberOfLevels* \[ à\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre de niveaux de mipmap (requiert également *MipLevel* ).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Il s’agit d’une liste des versions surchargées de cette méthode.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float NumberOfLevels);

void GetDimensions(out float Width);
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
