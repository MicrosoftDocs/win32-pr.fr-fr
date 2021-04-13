---
title: Accès à la bibliothèque par programmation
description: Accès à la bibliothèque par programmation
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Lecteur Windows Media, bibliothèque
- Modèle objet du lecteur Windows Media, bibliothèque
- modèle objet, bibliothèque
- Contrôle ActiveX du lecteur Windows Media, bibliothèque pour le modèle objet
- Contrôle ActiveX, bibliothèque pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, bibliothèque pour le modèle objet
- Windows Media Player Mobile, bibliothèque pour le modèle objet
- Bibliothèque du lecteur Windows Media, accès par programmation
- bibliothèque, accès
- accès à la bibliothèque du lecteur Windows Media par programmation
- Bibliothèque du lecteur Windows Media, ajout d’éléments multimédias
- bibliothèque, ajout d’éléments multimédias
- Bibliothèque du lecteur Windows Media, récupération d’éléments multimédias
- bibliothèque, récupération d’éléments multimédias
- Bibliothèque du lecteur Windows Media, suppression d’éléments multimédias
- bibliothèque, suppression d’éléments multimédias
- Ajout d’éléments multimédias à la bibliothèque du lecteur Windows Media
- récupération d’éléments multimédias à partir de la bibliothèque du lecteur Windows Media
- suppression d’éléments multimédias de la bibliothèque du lecteur Windows Media
- récupération de métadonnées
- Bibliothèque du lecteur Windows Media, récupération des métadonnées à partir des éléments multimédias
- bibliothèque, récupération de métadonnées à partir d’éléments multimédias
- métadonnées, récupération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380146"
---
# <a name="accessing-the-library-programmatically"></a>Accès à la bibliothèque par programmation

Dans le code, la bibliothèque est représentée par l’objet **MediaCollection** (ou l’interface **IWMPMediaCollection** ). Les éléments multimédias sont représentés en tant qu’objets **multimédias** (ou par l’interface **IWMPMedia** ). Les éléments de sélection sont représentés en tant qu’objets de **sélection** (ou par l’interface **IWMPPlaylist** ). Par souci de simplicité, cette section fait simplement référence aux noms d’objets, lorsque cela est possible.

À l’aide de l’objet **MediaCollection** , vous pouvez travailler avec des éléments multimédias et des sélections. La bibliothèque expose également l’objet **PlaylistCollection** (ou l’interface **IWMPPlaylistCollection** ), qui fournit certaines fonctionnalités spécifiques à l’utilisation des sélections. La plupart du temps, l’objet **MediaCollection** vous fournit les fonctionnalités dont vous avez besoin, même lorsque vous travaillez avec des sélections. Pour plus d’informations sur l’utilisation des éléments multimédias, consultez [gestion des éléments multimédias](managing-media-items.md). Pour plus d’informations sur l’utilisation des sélections, consultez [gestion des sélections](managing-playlists.md).

## <a name="adding-media-items-to-the-library"></a>Ajout d’éléments multimédias à la bibliothèque

L’ajout de contenu multimédia numérique à la bibliothèque est simple. Appelez simplement la méthode [MediaCollection. Add](mediacollection-add.md) , en fournissant le chemin d’accès au fichier multimédia en tant qu’argument.

## <a name="retrieving-media-items-from-the-library"></a>Récupération d’éléments multimédias à partir de la bibliothèque

Lorsque vous récupérez des éléments multimédias à partir de la bibliothèque, ce que vous récupérez vraiment est une sélection. Même si vous envisagez de récupérer un seul élément multimédia, vous obtiendrez un objet de **sélection** contenant un seul élément, qui sera associé à l’index zéro. Par exemple, si vous souhaitez récupérer un objet **multimédia** qui représente la chanson nommée « Jeanne », vous pouvez utiliser le code JScript suivant :


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



Le code précédent récupère une sélection contenant tous les éléments multimédias portant le nom « Jeanne » comme titre. Pour cet exemple, supposons que vous savez qu’il n’existe qu’une seule chanson par ce nom dans la bibliothèque (Notez que la bibliothèque prend en charge plusieurs chansons portant le même nom). Cela signifie que vous pouvez vous attendre à ce que le nombre d’éléments dans la sélection que vous avez récupéré soit égal à un et que l’élément multimédia soit représenté par l’index zéro. L’exemple de code suivant poursuit l’exemple précédent pour illustrer la façon dont vous récupérez l’élément multimédia à partir de la sélection à l’aide de la méthode [playlist. Item](playlist-item.md) .


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



Pour plus d’informations sur la récupération d’éléments multimédias à partir de sélections, consultez [sélections et éléments multimédias](playlists-and-media-items.md) dans le [Guide de contrôle du lecteur](player-control-guide.md).

## <a name="retrieving-metadata-from-a-media-item"></a>Récupération de métadonnées d’un élément multimédia

Après avoir récupéré un objet **multimédia** , vous pouvez lire les valeurs d’attribut associées au contenu. Dans le cas le plus simple, vous souhaiterez simplement connaître une seule valeur, telle que le nom de l’artiste qui a effectué une piste musicale. L’exemple JScript suivant montre comment utiliser la méthode [Media. getItemInfo](media-getiteminfo.md) pour récupérer le nom de l’artiste à partir du média récupéré dans l’exemple précédent :


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



Un élément multimédia peut avoir de nombreux attributs différents et l’utilisation des métadonnées n’est pas toujours aussi simple que le cas simple indiqué dans l’exemple précédent. Par exemple, certains attributs peuvent contenir plusieurs valeurs ou avoir des valeurs dans plusieurs langues. Pour plus d’informations sur l’utilisation des métadonnées, consultez [attributs d’élément multimédia](media-item-attributes.md). Pour plus d’informations sur les différents attributs, leurs significations et la prise en charge des types de fichiers, consultez la [référence d’attribut](attribute-reference.md).

## <a name="removing-media-items-from-the-library"></a>Suppression d’éléments multimédias de la bibliothèque

La suppression du contenu multimédia numérique de la bibliothèque est également simple. Appelez simplement **MediaCollection. Remove**, en fournissant l’objet **multimédia** qui représente l’élément comme premier argument et la valeur **true** comme deuxième argument. L’exemple JScript suivant supprime le fichier nommé Jeanne (récupéré dans l’exemple précédent) de la bibliothèque :


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos de la bibliothèque**](about-the-library.md)
</dt> <dt>

[**À propos des objets MediaCollection et Media**](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[**À propos des objets playlist, PlaylistCollection et PlaylistArray**](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[**Utilisation de la bibliothèque**](working-with-the-library.md)
</dt> </dl>

 

 




