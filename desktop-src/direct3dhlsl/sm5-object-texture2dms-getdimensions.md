---
title: 'Texture2DMS :: GetDimensions,, fonction'
description: 'Retourne les dimensions de la ressource. | Texture2DMS :: GetDimensions,, fonction'
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
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
ms.openlocfilehash: f720a10ac73f48ce1f27c5676d706a75178aa8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953631"
---
# <a name="texture2dmsgetdimensions-function"></a>Texture2DMS :: GetDimensions,, fonction

Retourne les dimensions de la ressource.

## <a name="syntax"></a>Syntaxe

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
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

*NumberOfSamples* \[ à\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’emplacements d’échantillonnage.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Il s’agit d’une liste des versions surchargées de cette méthode.


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
