---
title: Utilisation de sélections automatiques pour organiser le contenu de la bibliothèque
description: Utilisation de sélections automatiques pour organiser le contenu de la bibliothèque
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Lecteur Windows Media des magasins en ligne, sélections automatiques
- magasins en ligne, sélections automatiques
- tapez 1 magasins en ligne, sélections automatiques
- tapez 2 magasins en ligne, sélections automatiques
- Lecteur Windows Media des magasins en ligne, organisation du contenu de la bibliothèque
- magasins en ligne, organiser le contenu de la bibliothèque
- tapez 1 magasins en ligne, organiser le contenu de la bibliothèque
- tapez 2 magasins en ligne, organiser le contenu de la bibliothèque
- Lecteur Windows Media des magasins en ligne, organisation du contenu de la bibliothèque
- magasins en ligne, organisation du contenu de la bibliothèque
- types 1 magasins en ligne, organisation du contenu de la bibliothèque
- type 2 magasins en ligne, organisation du contenu de la bibliothèque
- bibliothèque, organisation du contenu
- Organisation du contenu de la bibliothèque
- sélections automatiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010852"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a>Utilisation de sélections automatiques pour organiser le contenu de la bibliothèque

Vous pouvez utiliser les sélections automatiques pour organiser le contenu Premium que vous fournissez. par exemple, vous pouvez utiliser Lecteur Windows Media pour créer une sélection automatique qui contient uniquement le contenu que vous avez fourni avec un classement utilisateur d’au moins quatre étoiles. vous pouvez ensuite ajouter la sélection automatique à la bibliothèque dans Lecteur Windows Media afin qu’elle s’affiche dans le nœud Musique acheté sous le nœud serveur de distribution de contenu.

Pour ce faire, procédez comme suit :

1.  Créez la sélection automatique.
2.  à l’aide de l’explorateur de Windows, accédez à la sélection automatique et récupérez le fichier. wpl.
3.  à l’aide du modèle objet Lecteur Windows Media, ajoutez la sélection automatique à la bibliothèque.
4.  Définissez l’attribut **WM/ContentDistributor** pour la sélection sur le nom de votre clé de serveur de distribution de contenu.
5.  Affectez à l’attribut **SyncOnly** de la playlist la valeur true.

l’exemple de code JScript suivant illustre une fonction qui ajoute une sélection automatique nommée « correspondances favorites » au nœud proseware dans la bibliothèque :


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’intégration de bibliothèque](download-manager-overview.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**MediaCollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Playlist. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Sélections statiques et automatiques**](static-and-auto-playlists.md)
</dt> <dt>

[**Attribut SyncOnly**](synconly-attribute.md)
</dt> <dt>

[**Attribut WM/ContentDistributor**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Utilisation de la bibliothèque**](working-with-the-library.md)
</dt> </dl>

 

 




