---
title: IWMPPlaylist. attributeName (VB et C)
description: La propriété attributeName (la \_ méthode obtenir AttributeName dans C \) obtient le nom d’un attribut playlist spécifié par un index.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist. attributeName (VB et C) lecteur Windows Media
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529660"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a>IWMPPlaylist. attributeName (VB et C#)

La propriété **AttributeName** (la méthode **obtenir \_ AttributeName** en C#) obtient le nom d’un attribut playlist spécifié par un index.


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a>Paramètres

*lIndex*

**System. Int32** qui est l’index de l’attribut playlist.

## <a name="return-value"></a>Valeur renvoyée

**System. String** qui est le nom de l’attribut playlist.

## <a name="remarks"></a>Notes

**IWMPPlaylist. AttributeName** est une propriété en lecture seule dans Visual Basic qui accepte un paramètre, tandis que en C#, elle est appelée méthode **IWMPPlaylist. obtenir \_ AttributeName** .

Le nombre d’attributs associés à une sélection est retourné par la propriété **IWMPPlaylist. attributeCount** .

Le nom retourné par cette propriété peut être fourni aux méthodes **setItemInfo** ou **getItemInfo** pour spécifier ou récupérer une valeur pour l’attribut nommé.

Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence des attributs](attribute-reference.md).

## <a name="examples"></a>Exemples

Consultez la propriété [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) pour obtenir un exemple de code qui utilise cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. attributeCount (VB et C#)**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. getItemInfo (VB et C#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. setItemInfo (VB et C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





