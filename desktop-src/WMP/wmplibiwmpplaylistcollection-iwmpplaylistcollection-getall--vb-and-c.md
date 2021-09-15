---
title: IWMPPlaylistCollection getAll, méthode
description: La méthode getAll retourne une interface IWMPPlaylistArray qui fournit l’accès à toutes les playlists de la bibliothèque.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- getAll, méthode Lecteur Windows Media
- getAll, méthode Lecteur Windows Media, IWMPPlaylistCollection, interface
- Lecteur Windows Media de l’interface IWMPPlaylistCollection, méthode getAll
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411289"
---
# <a name="iwmpplaylistcollectiongetall-method"></a>IWMPPlaylistCollection :: getAll, méthode

La méthode **GetAll** retourne une interface **IWMPPlaylistArray** qui fournit l’accès à toutes les playlists de la bibliothèque.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Interface **wmplib. IWMPPlaylistArray** pour le tableau de sélections récupéré.

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                                                     |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPPlaylistArray (VB et C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB et C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





