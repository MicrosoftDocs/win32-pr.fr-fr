---
title: Interface IWMPPlaylistCollection (VB et C) (WMP. h)
description: Fournit des méthodes pour manipuler des interfaces IWMPPlaylist et IWMPPlaylistArray dans une collection.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- IWMPPlaylistCollection (VB et C) interface Windows Media Player
- Interface IWMPPlaylistCollection (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc97f9e98838fedc3bd5441d6bfda2da5319dd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525966"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a>Interface IWMPPlaylistCollection (VB et C#)

Fournit des méthodes pour manipuler des interfaces **IWMPPlaylist** et **IWMPPlaylistArray** dans une collection.

## <a name="members"></a>Membres

L’interface **IWMPPlaylistCollection (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMPPlaylistCollection (VB et C#)** possède ces méthodes.



| Méthode                                                                                                 | Description                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**getAll**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | Retourne une interface **IWMPPlaylistArray** qui fournit l’accès à toutes les playlists de la bibliothèque.<br/>             |
| [**getByName**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | Retourne une interface **IWMPPlaylistArray** qui fournit l’accès aux sélections portant le nom spécifié, le cas échéant.<br/> |
| [**importPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | Ajoute une sélection statique à la bibliothèque.<br/>                                                                              |
| [**isDeleted**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | Retourne une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.<br/>                           |
| [**newPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | Retourne une interface **IWMPPlaylist** pour une nouvelle playlist vide dans la bibliothèque.<br/>                                     |
| [**Installez**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | Supprime une sélection de la bibliothèque.<br/>                                                                                |
| **setDeleted**                                                                                         | N'est plus pris en charge.<br/>                                                                                                |



 

Procurez-vous une interface **IWMPPlaylistCollection** à l’aide de la propriété suivante.



| Object                                                                   | Propriété                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Objet AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**playlistCollection**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistArray (VB et C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





