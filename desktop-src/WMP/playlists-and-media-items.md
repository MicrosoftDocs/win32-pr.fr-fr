---
title: Sélections et éléments multimédias
description: Sélections et éléments multimédias
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Lecteur Windows Media, sélections
- Lecteur Windows Media modèle objet, playlists
- modèle objet, sélections
- Lecteur Windows Media Mobile, sélections
- contrôle de ActiveX Lecteur Windows Media, sélections
- Lecteur Windows Media contrôle de ActiveX Mobile, sélections
- contrôle de ActiveX, sélections
- sélections, éléments multimédias
- sélections de métafichiers, éléments multimédias
- Windows Sélections de métafichiers multimédia, éléments multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292926"
---
# <a name="playlists-and-media-items"></a>Sélections et éléments multimédias

Une sélection est un ensemble d’éléments multimédias. Un objet **playlist** peut manipuler les objets **multimédia** qui représentent ces éléments.

## <a name="retrieving-media-items"></a>Récupération d’éléments multimédias

Pour une sélection existante, vous pouvez lire la *sélection*. propriété **Count** pour déterminer le nombre d’éléments multimédias présents dans la sélection, et vous pouvez obtenir une référence à l’objet **Media** correspondant à un élément spécifique à l’aide de la *sélection*. propriété **Item** .

L’exemple C# suivant récupère une référence d’objet à un élément multimédia spécifique. (Tout au long de cette rubrique, la variable *plist* est une référence à un objet **playlist** .)


```C++
currMedia = pList.Item(0);

```



L’exemple C# suivant récupère les noms de tous les éléments multimédias dans une sélection et les place dans une zone de liste nommée lstOutput.


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a>Ajout d’éléments à une sélection

Vous pouvez ajouter un élément multimédia à la fin d’une sélection ou à une position spécifique dans une sélection, à l’aide de la *sélection*. **appendItem** et *playlist*. méthodes **InsertItem** .

Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



L’exemple C# suivant illustre les deux techniques en ajoutant l’élément multimédia actuel à une sélection nommée « BluesTest », tout d’abord à la fin, puis au début de la sélection.


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



Lorsque vous créez une nouvelle playlist vide à l’aide de *PlaylistCollection*. méthode **newPlaylist** . vous pouvez y ajouter des éléments multimédias en appelant de manière répétée la *sélection*. méthode **appendItem** .

## <a name="manipulating-media-items-in-a-playlist"></a>Manipulation d’éléments multimédias dans une sélection

Vous pouvez modifier la position d’un élément multimédia dans la sélection à l’aide de la *sélection*. méthode **moveItem** . Vous spécifiez l’élément par son index actuel, puis vous spécifiez le nouvel index. L’exemple C# suivant déplace un élément de l’index 5 vers l’index 0 dans une sélection.


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



Vous pouvez supprimer un élément multimédia de la sélection à l’aide de la **sélection**. méthode **RemoveItem** . Notez que si l’élément supprimé n’était pas le dernier élément de la sélection, les valeurs d’index des éléments suivants changent. L’exemple C# suivant supprime l’élément spécifié.


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> Les utilisateurs peuvent modifier le contenu d’une sélection en dehors de votre application. chaque fois que vous manipulez les éléments d’une sélection, vous devez surveiller et gérer les événements liés aux playlists du contrôle Lecteur Windows Media pour vous assurer que votre code fonctionne correctement. Ces événements sont *Player*. **CurrentPlaylistChange** et *Player*. **PlaylistChange**.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des sélections**](managing-playlists.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> </dl>

 

 




