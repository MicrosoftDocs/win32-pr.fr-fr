---
title: Sélections statiques et automatiques
description: Sélections statiques et automatiques
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Lecteur Windows Media, sélections
- Modèle objet du lecteur Windows Media, sélections
- modèle objet, sélections
- Windows Media Player Mobile, sélections
- Contrôle ActiveX du lecteur Windows Media, sélections
- Contrôle ActiveX mobile du lecteur Windows Media, sélections
- Contrôle ActiveX, sélections
- sélections, statiques
- sélections de métafichiers, statiques
- Sélections de métafichiers Windows Media, statiques
- sélections statiques
- sélections automatiques
- sélections, auto
- sélections de métafichiers, auto
- Sélections de métafichiers Windows Media, auto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379687"
---
# <a name="static-and-auto-playlists"></a>Sélections statiques et automatiques

Il existe deux types de sélections :

-   Sélections statiques, qui incluent des éléments multimédias spécifiques
-   Les sélections automatiques, qui recherchent la bibliothèque à chaque ouverture et peuvent contenir différents éléments multimédias à des moments différents. Une sélection automatique est le résultat d’une requête de base de données.

Pour importer une playlist statique à partir d’un métafichier, appelez tout d’abord le *joueur*. **newPlaylist** pour créer un objet **playlist** basé sur les données du métafichier, puis passer cet objet à *PlaylistCollection*. **importPlaylist** pour ajouter la sélection à la bibliothèque.

Pour importer une sélection automatique à partir d’un métafichier, utilisez *MediaCollection*. **Ajoutez**. Pour plus d’informations, consultez [playlists et l’objet MediaCollection](playlists-and-the-mediacollection-object.md).

Pour importer une sélection statique à partir d’un métafichier de sélection automatique, utilisez le *lecteur*. **newPlaylist** et *PlaylistCollection*. **importPlaylist** comme décrit précédemment. La sélection automatique est exécutée une fois et une sélection statique est créée en fonction du résultat de cette exécution.

L’utilisation d’une sélection automatique pour interroger la bibliothèque de l’utilisateur n’est pas prise en charge pour les pages Web auxquelles les utilisateurs accèdent via Internet.

L’exemple de code C# suivant illustre l’importation d’un métafichier de sélection automatique en tant que sélection statique. Pour exécuter cet exemple, créez une sélection automatique à l’aide de l’interface utilisateur de la bibliothèque, puis incluez le chemin d’accès correct au métafichier de sélection automatique dans ce code.


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des sélections**](managing-playlists.md)
</dt> </dl>

 

 




