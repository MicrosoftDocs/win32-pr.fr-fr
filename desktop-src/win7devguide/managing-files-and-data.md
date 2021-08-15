---
title: Gestion des fichiers et des données
description: les utilisateurs ont un accès plus facile aux fichiers et aux données dans Windows 7.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9091a2d9bb2cf01d4f9b514c55e78f2f989f01d6d64a929608e14c32bfd395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086658"
---
# <a name="managing-files-and-data"></a>Gestion des fichiers et des données

les utilisateurs ont un accès plus facile aux fichiers et aux données dans Windows 7. les nouvelles api rendent les fichiers et les affichages plus instructifs, ce qui permet aux applications de fournir des informations pertinentes et distinctives à Windows Explorer. En outre, les applications tirent parti du nouveau modèle de *bibliothèque* , une notion utile et plus abstraite de l’espace de stockage utilisateur par rapport aux dossiers, et peuvent également participer à des bibliothèques communes de types de fichiers similaires partagés par différentes applications.

## <a name="libraries"></a>Bibliothèques

Windows 7 introduit le concept de *bibliothèques* comme des destinations où les développeurs et les utilisateurs finaux peuvent rechercher et organiser leurs données sous forme de collections d’éléments qui peuvent s’étendre sur plusieurs emplacements sur l’ordinateur local et sur des ordinateurs distants.

Les API de *bibliothèque* permettent aux développeurs de créer facilement des applications qui créent, interagissent avec et prennent en charge les *bibliothèques* en tant qu’éléments de première classe dans les applications. Vous pouvez également sélectionner des *bibliothèques* à l’aide de la boîte de dialogue Sélecteur de dossiers. Les applications peuvent énumérer les étendues de bibliothèque pertinentes, ou elles peuvent utiliser la bibliothèque directement en tant que dossier. (consultez [Windows bibliothèques](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) et les [bibliothèques Windows 7 : ressources](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)pour les développeurs).

![bibliothèque d’images Windows 7](images/windows7-10.jpg)

La *bibliothèque d’images* affiche vos images, quel que soit l’endroit où elles sont stockées

## <a name="file-formats-and-data-stores"></a>Formats de fichiers et banques de données

dans Windows 7, Windows Explorer facilite la gestion et la manipulation des fichiers pour l’utilisateur de plusieurs façons :

-   La version préliminaire du type de fichier de votre application est plus accessible à l’aide d’un nouveau bouton qui permet aux utilisateurs d’afficher et de masquer le volet de visualisation.
-   Les piles visuelles immersifs agrègent les images miniatures pour les types de fichiers dans une vue.
-   Windows Les vues de l’Explorateur affichent des informations utiles basées sur les propriétés écrites avec votre gestionnaire de propriétés.
-   Les extraits de document et la mise en surbrillance utilisent votre implémentation d’interface **IFilter** pour faciliter la recherche et la recherche de fichiers.
-   Les verbes et les commandes de menu contextuel sont plus faciles à implémenter.

En implémentant tous les gestionnaires de format appropriés pour les éléments retournés à partir de votre gestionnaire de protocole, les résultats de la recherche à partir de votre magasin de données personnalisé peuvent être aussi riches que les résultats de recherche de fichiers. Les *bibliothèques* sont automatiquement créées pour vos gestionnaires de protocole afin que les utilisateurs puissent facilement étendre leurs recherches. La logique de création de *bibliothèques* peut être facilement personnalisée via le registre. (voir [développement de filtres pour la recherche de Windows](../search/-search-3x-wds-extidx-filters.md).)

![bibliothèque de documents Windows 7](images/windows7-11.jpg)

dans Windows 7, Windows Explorer facilite la gestion et la manipulation des fichiers

 

 