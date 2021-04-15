---
title: Utilisation de sélections automatiques pour organiser le contenu de la bibliothèque
description: Utilisation de sélections automatiques pour organiser le contenu de la bibliothèque
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player Online stores, sélections automatiques
- magasins en ligne, sélections automatiques
- tapez 1 magasins en ligne, sélections automatiques
- tapez 2 magasins en ligne, sélections automatiques
- Windows Media Player Online stores, organiser le contenu de la bibliothèque
- magasins en ligne, organiser le contenu de la bibliothèque
- tapez 1 magasins en ligne, organiser le contenu de la bibliothèque
- tapez 2 magasins en ligne, organiser le contenu de la bibliothèque
- Magasins en ligne du lecteur Windows Media, organisation du contenu de la bibliothèque
- magasins en ligne, organisation du contenu de la bibliothèque
- types 1 magasins en ligne, organisation du contenu de la bibliothèque
- type 2 magasins en ligne, organisation du contenu de la bibliothèque
- bibliothèque, organisation du contenu
- Organisation du contenu de la bibliothèque
- sélections automatiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507299"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a>Utilisation de sélections automatiques pour organiser le contenu de la bibliothèque

Vous pouvez utiliser les sélections automatiques pour organiser le contenu Premium que vous fournissez. Par exemple, vous pouvez utiliser le lecteur Windows Media pour créer une sélection automatique qui contient uniquement le contenu que vous avez fourni avec un classement utilisateur d’au moins quatre étoiles. Vous pouvez ensuite ajouter la sélection automatique à la bibliothèque dans le lecteur Windows Media pour qu’elle s’affiche dans le nœud musique achetée sous le nœud serveur de distribution de contenu.

Pour ce faire, procédez comme suit :

1.  Créez la sélection automatique.
2.  À l’aide de l’Explorateur Windows, accédez à la sélection automatique et récupérez le fichier. wpl.
3.  À l’aide du modèle objet du lecteur Windows Media, ajoutez la sélection automatique à la bibliothèque.
4.  Définissez l’attribut **WM/ContentDistributor** pour la sélection sur le nom de votre clé de serveur de distribution de contenu.
5.  Affectez à l’attribut **SyncOnly** de la playlist la valeur true.

L’exemple de code JScript suivant illustre une fonction qui ajoute une sélection automatique nommée « correspondances favorites » au nœud Proseware dans la bibliothèque :


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

 

 




