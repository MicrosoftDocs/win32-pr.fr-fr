---
title: Sélections et objet PlaylistCollection
description: Sélections et objet PlaylistCollection
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Lecteur Windows Media, sélections
- Lecteur Windows Media modèle objet, playlists
- modèle objet, sélections
- Lecteur Windows Media Mobile, sélections
- contrôle de ActiveX Lecteur Windows Media, sélections
- Lecteur Windows Media contrôle de ActiveX Mobile, sélections
- contrôle de ActiveX, sélections
- sélections, objet PlaylistCollection
- sélections de métafichiers, objet PlaylistCollection
- Windows Sélections de métafichiers multimédia, objet PlaylistCollection
- Objet PlaylistCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98744c2c5b97129db2824c42567802a374f90b6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292911"
---
# <a name="playlists-and-the-playlistcollection-object"></a>Sélections et objet PlaylistCollection

L’objet **PlaylistCollection** vous donne accès aux sélections de la bibliothèque et contient des méthodes permettant de créer de nouvelles playlists vides et de nouvelles sélections à partir des fichiers de la bibliothèque.

## <a name="working-with-existing-playlists"></a>Utilisation des sélections existantes

*PlaylistCollection*. **GetAll** et *PlaylistCollection*. les méthodes **GetByName** retournent chacune un objet **PlaylistArray** , qui peut contenir plusieurs sélections.

*PlaylistCollection*. la méthode **GetAll** retourne toutes les playlists existantes qui se trouvent dans la bibliothèque. Par exemple, vous pouvez appeler cette méthode, puis récupérer les sélections dans l’objet **PlaylistArray** pour déterminer si un nom de playlist donné a déjà été utilisé, ou pour afficher toutes les playlists de l’utilisateur. L’exemple de code dans les [attributs de sélection](playlist-attributes.md) utilise la méthode **GetAll** .

*PlaylistCollection*. la méthode **GetByName** retourne toutes les sélections avec un nom donné. Vous pouvez utiliser cette méthode pour gérer chacune de ces sélections séparément.

Vous pouvez également utiliser la méthode **GetByName** pour récupérer une sélection unique par nom. Dans ce cas, l’objet **PlaylistArray** n’a qu’un seul élément. L’exemple C# suivant illustre cette technique.


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a>Utilisation de nouvelles sélections

Vous pouvez utiliser *PlaylistCollection*. méthode **newPlaylist** pour créer une nouvelle playlist vide. La méthode retourne une référence au nouvel objet **playlist** . Vous pouvez ensuite appeler la *sélection*. méthode **appendItem** pour ajouter des éléments multimédias à la sélection.

Vous pouvez également créer une nouvelle sélection basée sur un métafichier de sélection. Tout d’abord, transmettez le nom de la sélection et le chemin d’accès au métafichier au *joueur*. méthode **newPlaylist** . Cette méthode retourne une référence au nouvel objet **playlist** . Ensuite, transmettez le nouvel objet **playlist** à *PlaylistCollection*. méthode **importPlaylist** pour l’ajouter à la bibliothèque.

Notez la différence entre les *PlaylistCollection*. méthode **newPlaylist** et *Player*. méthode **newPlaylist** . La méthode **PlaylistCollection** crée une nouvelle playlist vide et l’ajoute à la bibliothèque. La méthode **Player** crée un nouvel objet de **sélection** rempli, mais ne l’ajoute pas à la bibliothèque.

Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



L’exemple C# suivant illustre l’importation d’une sélection à partir d’un métafichier. L’argument *strPListName* spécifie le nom de la nouvelle sélection. *StrMetaFileName* spécifie le nom du métafichier à partir duquel la sélection est importée.


```C++
private IWMPPlaylist importPlaylist(string strPlaylistName, string strMetaFileName)
{
    IWMPPlaylist  NewPlaylist;
    IWMPPlaylist  ImportPlaylist;

    NewPlaylist = Player.newPlaylist(strPlaylistName, strMetaFileName);
    ImportPlaylist = Player.playlistCollection.importPlaylist(NewPlaylist);

    return ImportPlaylist;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des sélections**](managing-playlists.md)
</dt> <dt>

[**Player. newPlaylist**](player-newplaylist.md)
</dt> <dt>

[**Playlist. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Objet PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Objet PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Sélections et éléments multimédias**](playlists-and-media-items.md)
</dt> </dl>

 

 




