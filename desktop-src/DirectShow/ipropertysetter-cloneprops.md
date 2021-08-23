---
description: La méthode CloneProps clone un ensemble de propriétés à partir de cet accesseur Set de propriété et les ajoute à un nouvel accesseur Set de propriété.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'IPropertySetter :: CloneProps, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54dd2ad08334a0c61918de74396e62fcc21e095df81c2d773995b6cfbdddc19d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755919"
---
# <a name="ipropertysettercloneprops-method"></a>IPropertySetter :: CloneProps, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `CloneProps` méthode Clone un jeu de propriétés à partir de cet accesseur Set de propriété et les ajoute à un nouvel accesseur Set de propriété.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppSetter* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface **IPropertySetter** du nouvel accesseur Set de propriété.

</dd> <dt>

*rtStart* \[ dans\]
</dt> <dd>

Heure de début de la plage de valeurs à cloner, en unités de 100 nanosecondes.

</dd> <dt>

*rtStop* \[ dans\]
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Seules les valeurs qui tombent après l’heure de début spécifiée sont clonées. Les heures sur les valeurs clonées sont ensuite ajustées par rapport à l’heure de début. Par exemple, si *rtStart* est 20 millions (2 secondes), une valeur à l’heure 30 millions (3 secondes) est clonée avec l’heure 10 millions (1 seconde). Enfin, chaque propriété clonée reçoit une valeur initiale égale à la valeur de la propriété d’origine à l’heure de début (correctement interpolée si nécessaire). En effet, les données de propriété sont fractionnées à l’heure de début spécifiée.

Si la méthode est réussie, l’interface [**IPropertySetter**](ipropertysetter.md) qu’elle retourne a un nombre de références en suspens. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




