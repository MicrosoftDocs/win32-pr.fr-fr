---
title: 'Texture2DMSArray :: Load (int, int), fonction'
description: 'Obtient une valeur. | Texture2DMSArray :: Load (int, int), fonction'
ms.assetid: 955135cf-1bac-4d0c-9870-2b6d59d9dd88
keywords:
- Charger la fonction HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83da1a2af6ffc7e990ba1fd4c7f220387304c770
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922267"
---
# <a name="texture2dmsarrayloadintint-function"></a>Texture2DMSArray :: Load (int, int), fonction

Obtient une valeur.

## <a name="syntax"></a>Syntaxe

``` syntax
T Load(
  in int3 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Coord* \[ dans\]
</dt> <dd>

Type : **Int3**

Emplacement d’entrée.

</dd> <dt>

*sampleindex* \[ dans\]
</dt> <dd>

Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Exemple d’index.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **T**

Une valeur, dont le type correspond au type de modèle de texture.

## <a name="remarks"></a>Notes

Il s’agit d’une liste des versions surchargées de cette méthode.


```
void Load(in int3 coord,
  in int sampleindex,
  in int2 offset);
```



Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Méthodes Load](texture2dmsarray-load.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
