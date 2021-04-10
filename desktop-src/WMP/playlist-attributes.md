---
title: Attributs de sélection
description: Attributs de sélection
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Lecteur Windows Media, sélections
- Modèle objet du lecteur Windows Media, sélections
- modèle objet, sélections
- Windows Media Player Mobile, sélections
- Contrôle ActiveX du lecteur Windows Media, sélections
- Contrôle ActiveX mobile du lecteur Windows Media, sélections
- Contrôle ActiveX, sélections
- sélections, attributs
- sélections de métafichiers, attributs
- Sélections de métafichiers Windows Media, attributs
- attributs, sélections
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939834"
---
# <a name="playlist-attributes"></a>Attributs de sélection

Les sélections comportent des informations de métadonnées appelées attributs, tout comme les éléments multimédias ont des attributs. Vous pouvez récupérer les noms et les valeurs des attributs de sélection et les afficher dans votre interface utilisateur, ou votre code peut prendre des mesures en fonction de la valeur d’un attribut.

Les sélections sont définies dans des fichiers organisés dans un format XML, et des éléments particuliers du fichier définissent des attributs de sélection. Certains éléments d’attribut sont connus ; l’auteur du métafichier peut également définir des attributs arbitraires. Pour plus d’informations sur les éléments d’attribut dans les fichiers de sélection, consultez [récupération des métadonnées](retrieving-metadata.md).

La bibliothèque peut fournir des attributs de sélection supplémentaires, tels que **SourceURL** ou **UserLastPlayedTime**. Pour plus d’informations sur les attributs de sélection de bibliothèque, consultez la [référence](attribute-reference.md)des attributs du lecteur Windows Media.

*Sélection*. la propriété **attributeCount** récupère le nombre d’attributs associés à la sélection. *Sélection*. la propriété **AttributeName** récupère le nom d’un attribut en fonction de son index et de la *sélection*. la méthode **getItemInfo** récupère la valeur d’un attribut en fonction de son nom.

Vous pouvez modifier la valeur d’un attribut de la sélection actuelle avec la *sélection*. méthode **setItemInfo** .

Une utilisation spéciale de la méthode **setItemInfo** consiste à trier les éléments de la sélection, à l’aide de l’attribut **SortAttribute** . L’exemple C# suivant trie une sélection selon les valeurs de l’attribut **UserLastPlayedTime** . La *sélection* de variable est une référence à un objet **playlist** .


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



L’exemple de code C# suivant montre comment récupérer des attributs de sélection. La première fonction, ShowPlaylists, remplit un contrôle ListBox avec les noms des sélections disponibles. La deuxième partie est le gestionnaire d’événements de zone de liste. Quand l’utilisateur clique sur un nom de playlist, ce code récupère les attributs de cette playlist et affiche ces attributs dans une deuxième zone de liste.


```C++
// Member variables
IWMPPlaylistCollection PlaylistColl;
IWMPPlaylistArray PlaylistArray;

private void ShowPlaylists()
{
    // Retrieve the playlist collection
    PlaylistColl = Player.playlistCollection;
    // Store the collection in a playlist array
    PlaylistArray = PlaylistColl.getAll();

    // Retrieve the count of elements
    iCount = PlaylistArray.count;

    // Update the list box with the playlist names.
    lstPlaylist.BeginUpdate();
    for (int i=0; i<iCount; i++)
    {
        lstPlaylist.Items.Add(PlaylistArray.Item(i).name);
    }
    lstPlaylist.EndUpdate();

    // Set the selected index to zero
    lstPlaylist.SelectedIndex = 0;
}

```



L’événement SelectedIndexChanged du contrôle ListBox est appelé chaque fois que l’utilisateur sélectionne un nom de sélection. Le gestionnaire d’événements suivant remplit une deuxième zone de liste avec les noms d’attributs et les valeurs correspondant à la sélection de l’utilisateur.


```C++
private void lstPlaylist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    IWMPPlaylist Playlist = PlaylistArray.Item(lstPlaylist.SelectedIndex);
    string strAttr="";
    string strItemNames="";
    int iAttribCount=0;

    iAttribCount = Playlist.attribCount;
    for (j=0; j<iAttribCount; j++)
    {
        strAttr=Playlist.get_attributeName(j) + " -- ";
        strAttr+=Playlist.getItemInfo(Playlist.get_attributeName(j));
        lstOutput.Items.Add(strAttr);
    }
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des sélections**](managing-playlists.md)
</dt> <dt>

[**Attributs d’élément multimédia**](media-item-attributes.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> </dl>

 

 




