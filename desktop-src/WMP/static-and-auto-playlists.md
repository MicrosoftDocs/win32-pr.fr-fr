---
title: Sélections statiques et automatiques
description: Sélections statiques et automatiques
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Lecteur Windows Media, sélections
- Lecteur Windows Media modèle objet, playlists
- modèle objet, sélections
- Lecteur Windows Media Mobile, sélections
- contrôle de ActiveX Lecteur Windows Media, sélections
- Lecteur Windows Media contrôle de ActiveX Mobile, sélections
- contrôle de ActiveX, sélections
- sélections, statiques
- sélections de métafichiers, statiques
- Windows Sélections de métafichiers multimédias, statiques
- sélections statiques
- sélections automatiques
- sélections, auto
- sélections de métafichiers, auto
- Windows Sélections de métafichiers multimédias, auto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645b3bd9ca9ddeebcce9fd6cbb905caa54717e87876be6e449ebd4d3ab64a11a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568781"
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

 

 




