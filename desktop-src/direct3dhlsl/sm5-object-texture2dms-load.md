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
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974167"
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

## <a name="return-value"></a>Valeur retournée

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



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load](texture2dms-load.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
