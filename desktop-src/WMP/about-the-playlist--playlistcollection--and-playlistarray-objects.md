---
title: À propos des objets playlist, PlaylistCollection et PlaylistArray
description: À propos des objets playlist, PlaylistCollection et PlaylistArray
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Lecteur Windows Media, objet playlist
- Modèle objet du lecteur Windows Media, objet playlist
- modèle objet, objet playlist
- Contrôle ActiveX du lecteur Windows Media, objet playlist
- Contrôle ActiveX, objet playlist
- Contrôle ActiveX Windows Media Player Mobile, objet playlist
- Windows Media Player Mobile, objet playlist
- Objet playlist
- Lecteur Windows Media, objet PlaylistCollection
- Modèle objet du lecteur Windows Media, objet PlaylistCollection
- modèle objet, objet PlaylistCollection
- Contrôle ActiveX du lecteur Windows Media, objet PlaylistCollection
- Contrôle ActiveX, objet PlaylistCollection
- Contrôle ActiveX Windows Media Player Mobile, objet PlaylistCollection
- Windows Media Player Mobile, objet PlaylistCollection
- Objet PlaylistCollection
- Lecteur Windows Media, objet PlaylistArray
- Modèle objet du lecteur Windows Media, objet PlaylistArray
- modèle objet, objet PlaylistArray
- Contrôle ActiveX du lecteur Windows Media, objet PlaylistArray
- Contrôle ActiveX, objet PlaylistArray
- Contrôle ActiveX Windows Media Player Mobile, objet PlaylistArray
- Windows Media Player Mobile, objet PlaylistArray
- Objet PlaylistArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509797"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a>À propos des objets playlist, PlaylistCollection et PlaylistArray

Les objets **playlist**, **PlaylistCollection** et **PlaylistArray** régissent les sélections que le lecteur Windows Media peut utiliser pour spécifier l’ordre dans lequel le contenu est lu. Vous récupérez l’objet **PlaylistCollection** à partir de la propriété **PlaylistCollection** de l’objet **Player** . La propriété **playlistCollection** retourne l’objet **playlistCollection** . Vous pouvez uniquement accéder aux propriétés de l’objet **PlaylistCollection** après l’avoir créé. Par exemple, pour créer une nouvelle sélection, vous devez d’abord obtenir l’objet **PlaylistCollection** , puis utiliser une méthode sur cet objet.


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

 

 




