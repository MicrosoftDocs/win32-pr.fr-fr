---
title: Méthode IWMPPlaylistCollection importPlaylist
description: La méthode importPlaylist ajoute une sélection statique à la bibliothèque. | Méthode IWMPPlaylistCollection importPlaylist
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- Lecteur Windows Media de la méthode importPlaylist
- méthode importPlaylist Lecteur Windows Media, interface IWMPPlaylistCollection
- Lecteur Windows Media de l’interface IWMPPlaylistCollection, méthode importPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411284"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a>IWMPPlaylistCollection :: importPlaylist, méthode

La méthode **importPlaylist** ajoute une sélection statique à la bibliothèque.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*pItem* \[ dans\]
</dt> <dd>

Une interface **wmplib. IWMPPlaylist** pour la sélection que cette méthode ajoutera.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Interface **wmplib. IWMPPlaylist** pour la sélection ajoutée.

## <a name="remarks"></a>Notes

Les sélections qui ne contiennent pas d’éléments multimédias ne peuvent pas être ajoutées à la bibliothèque à l’aide de cette méthode. Pour créer une playlist vide dans la bibliothèque, utilisez la méthode **newPlaylist** . Vous pouvez ensuite remplir la playlist obtenue avec des éléments multimédias à l’aide de **IWMPPlaylist. appendItem** ou **IWMPPlaylist. InsertItem**.

Si vous transmettez cette méthode à une sélection automatique, la requête est exécutée une fois et le résultat est ajouté à la bibliothèque en tant que sélection statique. Pour ajouter une sélection automatique à la bibliothèque et conserver son comportement automatique, utilisez **IWMPMediaCollection. Add**. Pour plus d’informations, consultez [sélections statiques et automatiques](static-and-auto-playlists.md).

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                                                     |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMPMediaCollection. add (VB et C#)**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. appendItem (VB et C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB et C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB et C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. newPlaylist (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





