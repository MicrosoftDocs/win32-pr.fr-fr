---
title: Sélections et objet MediaCollection
description: Sélections et objet MediaCollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Lecteur Windows Media, sélections
- Lecteur Windows Media modèle objet, playlists
- modèle objet, sélections
- Lecteur Windows Media Mobile, sélections
- contrôle de ActiveX Lecteur Windows Media, sélections
- Lecteur Windows Media contrôle de ActiveX Mobile, sélections
- contrôle de ActiveX, sélections
- sélections, objet MediaCollection
- sélections de métafichiers, objet MediaCollection
- Windows Sélections de métafichiers multimédia, objet MediaCollection
- Objet MediaCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292915"
---
# <a name="playlists-and-the-mediacollection-object"></a>Sélections et objet MediaCollection

L’objet **MediaCollection** vous donne accès à diverses sélections spéciales et inclut une méthode pour créer une nouvelle sélection à partir d’un métafichier.

Les méthodes suivantes récupèrent des sélections spéciales :

-   **getAll**
-   **getByAlbum**
-   **getByAttribute**
-   **getByAuthor**
-   **getByGenre**
-   **getByName**

Comme leur nom le suggère, ces méthodes récupèrent les sélections contenant tous les éléments multimédias de la bibliothèque qui correspondent à certains critères.

Veillez à ne pas confondre le *MediaCollection*. méthode **GetByName** avec *PlaylistCollection*. méthode **GetByName** . La méthode **MediaCollection** retourne un objet **playlist** contenant tous les éléments multimédias portant le nom spécifié. La méthode **PlaylistCollection** retourne un objet **PlaylistArray** contenant toutes les sélections portant le nom spécifié.

Vous pouvez utiliser *MediaCollection*. **Ajoutez** une méthode pour ajouter des sélections ainsi que des éléments multimédias à la bibliothèque. Pour ajouter une sélection, vous transmettez à la méthode le chemin d’accès au métafichier qui définit la sélection. La méthode retourne toujours un objet **Media** . Vous ne pouvez pas effectuer un cast entre des objets de **média** et de **sélection** . Pour utiliser la sélection que vous avez ajoutée, récupérez l’objet de **sélection** portant le même nom que l’objet **multimédia** .

L’exemple C# suivant montre comment récupérer des médias par type à l’aide de **MediaCollection**. méthode **getByAttribute** . Ce code récupère les noms de tous les attributs associés à un type donné, ainsi que l’État en lecture/écriture ou en lecture seule de ces attributs. il génère un fichier unique qui contient des listes d’attributs pour les types Audio, vidéo, Radio, Playlist, Other, Musique et Photo.


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



L’exemple C# suivant montre comment ajouter une sélection d’un métafichier à la bibliothèque.


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



Les sélections statiques incluent des éléments multimédias spécifiques. Les sélections automatiques recherchent la bibliothèque à chaque fois qu’elles sont ouvertes et peuvent contenir différents éléments multimédias à des moments différents. Vous pouvez ajouter des sélections statiques et automatiques à la bibliothèque à l’aide de *MediaCollection*. **Ajouter** une méthode. Vous pouvez également ajouter des sélections statiques à l’aide de *PlaylistCollection*. méthode **importPlaylist** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des sélections**](managing-playlists.md)
</dt> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**Objet PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Sélections et objet PlaylistCollection**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**Sélections statiques et automatiques**](static-and-auto-playlists.md)
</dt> </dl>

 

 




