---
title: À propos des objets playlist, PlaylistCollection et PlaylistArray
description: À propos des objets playlist, PlaylistCollection et PlaylistArray
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Lecteur Windows Media, objet Playlist
- Lecteur Windows Media modèle objet, objet Playlist
- modèle objet, objet playlist
- contrôle de ActiveX Lecteur Windows Media, objet Playlist
- contrôle ActiveX, objet Playlist
- Lecteur Windows Media contrôle Mobile ActiveX, objet Playlist
- Lecteur Windows Media Mobile, objet playlist
- Objet playlist
- Lecteur Windows Media, objet PlaylistCollection
- Lecteur Windows Media modèle objet, objet PlaylistCollection
- modèle objet, objet PlaylistCollection
- Lecteur Windows Media ActiveX contrôle, objet PlaylistCollection
- contrôle ActiveX, objet PlaylistCollection
- Lecteur Windows Media contrôle Mobile ActiveX, objet PlaylistCollection
- Lecteur Windows Media Mobile, objet PlaylistCollection
- Objet PlaylistCollection
- Lecteur Windows Media, objet PlaylistArray
- Lecteur Windows Media modèle objet, objet PlaylistArray
- modèle objet, objet PlaylistArray
- Lecteur Windows Media ActiveX contrôle, objet PlaylistArray
- contrôle ActiveX, objet PlaylistArray
- Lecteur Windows Media contrôle Mobile ActiveX, objet PlaylistArray
- Lecteur Windows Media Mobile, objet PlaylistArray
- Objet PlaylistArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37a20bca66d8d1ff592b71d1f6555641625b4688b7791475a85f7b9a39fa91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956719"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a>À propos des objets playlist, PlaylistCollection et PlaylistArray

les objets **playlist**, **PlaylistCollection** et **PlaylistArray** régissent les sélections que Lecteur Windows Media pouvez utiliser pour spécifier l’ordre dans lequel le contenu est lu. Vous récupérez l’objet **PlaylistCollection** à partir de la propriété **PlaylistCollection** de l’objet **Player** . La propriété **playlistCollection** retourne l’objet **playlistCollection** . Vous pouvez uniquement accéder aux propriétés de l’objet **PlaylistCollection** après l’avoir créé. Par exemple, pour créer une nouvelle sélection, vous devez d’abord obtenir l’objet **PlaylistCollection** , puis utiliser une méthode sur cet objet.


```C++
player.playlistcollection.newplaylist('myplaylist');
```



Vous pouvez récupérer la sélection en cours à l’aide de la propriété **currentPlaylist** . Par exemple, pour obtenir le nom de la sélection actuelle, utilisez le code suivant :


```C++
myname = player.currentplaylist.name;
```



L’objet **PlaylistArray** est retourné par les méthodes **GetAll** et **GetByName** de l’objet **PlaylistCollection** . Pour obtenir le nombre de sélections, par exemple, utilisez le code suivant :


```C++
howmany = player.playlistcollection.getAll().count;
```



Pour récupérer une sélection connue par son nom, utilisez le code suivant :


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Modèle objet de lecteur pour les langages de script**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**Objet PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Objet PlaylistCollection**](playlistcollection-object.md)
</dt> </dl>

 

 




