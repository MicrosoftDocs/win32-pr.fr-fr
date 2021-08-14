---
title: 'Texture2DMS :: Load (int, int), fonction'
description: 'Obtient une valeur. | Texture2DMS :: Load (int, int), fonction'
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Charger la fonction DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0997a1bd30b4912864674015057fcafec227d90ad05b16b88fd3f05b671f155c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285727"
---
# <a name="texture2dmsloadintint-function"></a>Texture2DMS :: Load (int, int), fonction

Obtient une valeur.

## <a name="syntax"></a>Syntaxe

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Coord* \[ dans\]
</dt> <dd>

Type : **Int2**

Emplacement d’entrée.

</dd> <dt>

*sampleindex* \[ dans\]
</dt> <dd>

Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Exemple d’index.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **T**

Une valeur, dont le type correspond au type de modèle de texture.

## <a name="remarks"></a>Notes

Il s’agit d’une liste des versions surchargées de cette méthode.


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load](texture2dms-load.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
