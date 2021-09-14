---
title: Emplacement et élément sélectionné
description: Emplacement et élément sélectionné
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Lecteur Windows Media magasins en ligne, emplacements
- magasins en ligne, emplacements
- tapez 1 magasins en ligne, emplacements
- magasins en ligne Lecteur Windows Media, emplacements de bibliothèque
- magasins en ligne, emplacements de bibliothèque
- types 1 magasins en ligne, emplacements de bibliothèque
- Lecteur Windows Media des magasins en ligne, éléments sélectionnés
- magasins en ligne, éléments sélectionnés
- tapez 1 magasins en ligne, éléments sélectionnés
- bibliothèque de Lecteur Windows Media, emplacements
- bibliothèque de Lecteur Windows Media, éléments sélectionnés
- bibliothèque, emplacements
- bibliothèque, éléments sélectionnés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919235"
---
# <a name="location-and-selected-item"></a>Emplacement et élément sélectionné

Lecteur Windows Media utilise les cinq éléments suivants pour caractériser sa vue actuelle du contenu du magasin en ligne :

-   tâche
-   type d’emplacement de la bibliothèque
-   ID d’emplacement de la bibliothèque
-   type d’élément sélectionné
-   ID de l’élément sélectionné

en règle générale, vous pouvez considérer la vue dans Lecteur Windows Media comme un conteneur d’éléments. Le conteneur a un type et un élément a un type. Tous les éléments d’un conteneur ont le même type. Les types d’emplacement et les types d’élément sont spécifiés par les [constantes d’emplacement](library-location-constants.md)de la bibliothèque. Par exemple, si la vue actuelle affiche un album individuel, le type d’emplacement de la bibliothèque est CPAlbumID et, étant donné qu’un album contient des suivis, le type d’élément sélectionné est CPTrackID.

Le tableau suivant montre l’emplacement et les types d’éléments de plusieurs conteneurs.



| Description du conteneur                              | Type d’emplacement de la bibliothèque | Type d’élément sélectionné |
|-------------------------------------------------------|-----------------------|--------------------|
| Un album qui est un conteneur de pistes                | CPAlbumID             | CPTrackID          |
| Liste qui est un conteneur de pistes                  | CPListID              | CPTrackID          |
| Liste qui est un conteneur d’albums                  | CPListID              | CPAlbumID          |
| Station de radio qui est un conteneur de listes          | CPRadioID             | CPListID           |
| Ensemble de tous les albums, qui est un conteneur d’albums | AllCPAlbumIDs         | CPAlbumID          |
| Ensemble de tous les genres, qui est un conteneur de genres | AllCPGenreIDs         | CPGenreID          |



 

les onglets de Lecteur Windows Media représentent des tâches différentes. Le lecteur affiche le contenu de la boutique en ligne dans trois volets de tâches différents : **bibliothèque**, **gravure** et **synchronisation**. Le volet des tâches de la bibliothèque est également appelé volet des tâches **Parcourir** . Parfois, un volet de tâches est appelé *fonctionnalité*. vous pouvez donc voir des termes tels que la fonctionnalité de *gravure* et la *fonctionnalité de synchronisation* dans cette documentation.

les exemples suivants montrent comment Lecteur Windows Media utilise les cinq éléments d’informations (tâche, type d’emplacement de la bibliothèque, id d’emplacement de la bibliothèque, type d’élément sélectionné, id d’élément sélectionné) pour caractériser différentes vues.

Dans le volet de tâches **graver** , le lecteur affiche un album en tant que conteneur de pistes. L’ID de l’album est 250. Dans la vue, l’élément sélectionné est la piste qui a l’ID 800. Notez que 800 est l’ID de la piste dans le catalogue du magasin en ligne, et non le numéro de la piste sur l’album.



| Élément                  | Valeur     |
|-----------------------|-----------|
| tâche                  | Écrire      |
| type d’emplacement de la bibliothèque | CPAlbumID |
| ID d’emplacement de la bibliothèque   | 250       |
| type d’élément sélectionné    | CPTrackID |
| ID de l’élément sélectionné      | 800       |



 

Dans le volet de tâches **synchroniser** , le lecteur affiche l’ensemble de tous les albums, qui est un conteneur d’albums. Dans la vue, l’élément sélectionné est l’album dont l’ID est 300. Notez que l’ID d’emplacement de la bibliothèque n’est pas applicable à cette vue.



| Élément                  | Valeur         |
|-----------------------|---------------|
| tâche                  | Synchronisation          |
| type d’emplacement de la bibliothèque | AllCPAlbumIDs |
| ID d’emplacement de la bibliothèque   | N/A           |
| type d’élément sélectionné    | CPAlbumID     |
| ID de l’élément sélectionné      | 300           |



 

Dans le contrôle Tree-View, le nœud racine du magasin en ligne est sélectionné. Dans ce cas, il n’y a aucun conteneur et, par conséquent, il n’y a aucun élément. Le volet des tâches **bibliothèque** complète affiche une page de détection.



| Élément                  | Valeur           |
|-----------------------|-----------------|
| tâche                  | Parcourir          |
| type d’emplacement de la bibliothèque | RootLocation    |
| ID d’emplacement de la bibliothèque   | N/A             |
| type d’élément sélectionné    | UnknownLocation |
| ID de l’élément sélectionné      | N/A             |



 

Dans le volet de tâches **synchronisation** , le lecteur affiche l’année 2002 en tant que conteneur de pistes. Dans la vue, l’élément sélectionné est la piste qui a l’ID 450.



| Élément                  | Valeur           |
|-----------------------|-----------------|
| tâche                  | Synchronisation            |
| type d’emplacement de la bibliothèque | ReleaseDateYear |
| ID d’emplacement de la bibliothèque   | 2002            |
| type d’élément sélectionné    | CPTrackID       |
| ID de l’élément sélectionné      | 450             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Pages de découverte**](discovery-pages.md)
</dt> </dl>

 

 




