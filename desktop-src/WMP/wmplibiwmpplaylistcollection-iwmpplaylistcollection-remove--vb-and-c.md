---
title: IWMPPlaylistCollection méthode Remove
description: La méthode Remove supprime une sélection de la bibliothèque. | IWMPPlaylistCollection méthode Remove
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- Méthode Remove Windows Media Player
- Remove, méthode lecteur Windows Media, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection lecteur Windows Media, méthode Remove
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525677"
---
# <a name="iwmpplaylistcollectionremove-method"></a>IWMPPlaylistCollection :: Remove, méthode

La méthode **Remove** supprime une sélection de la bibliothèque.

## <a name="syntax"></a>Syntaxe


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*pItem* \[ dans\]
</dt> <dd>

Une interface **wmplib. IWMPPlaylist** pour la sélection que cette méthode supprimera.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                                                     |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB et C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





