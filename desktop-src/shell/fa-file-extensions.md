---
description: L’inscription d’un type de fichier est la première étape de la création d’une association de fichiers, ce qui rend ce type de fichier &\# 0034 ; connu&\# 0034 ; dans le shell. Toutefois, sans gestionnaires de type de fichier, l’interpréteur de commandes ne peut pas exposer d’informations à l’utilisateur à partir du fichier.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Gestionnaires de types de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862366"
---
# <a name="file-type-handlers"></a>Gestionnaires de types de fichiers

L' [inscription d’un type de fichier](fa-how-work.md) est la première étape de la création d’une association de fichiers, ce qui rend ce type de fichier « connu » pour l’interpréteur de commandes. Toutefois, sans gestionnaires de type de fichier, l’interpréteur de commandes ne peut pas exposer d’informations à l’utilisateur à partir du fichier.

Cette rubrique est organisée comme suit :

-   [Rendre un type de fichier connu de l’interpréteur de commandes](#make-a-file-type-known-to-shell)
-   [Description du gestionnaire de types de fichiers](#file-type-handler-descriptions)
-   [Rubriques connexes](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>Rendre un type de fichier connu de l’interpréteur de commandes

Dans la capture d’écran suivante de l’Explorateur Windows, le fichier image désert. connu apparaît dans la bibliothèque d' **images** de Shell et est associé uniquement à l’application Paint.

![capture d’écran montrant l’Explorateur ouverture d’une image sans type de fichier](images/file-assoc/fileassoc-filetypehandler.png)

Le fichier désert. connu dans la capture d’écran précédente ne dispose pas des fonctionnalités suivantes qui sont activées par un gestionnaire de type de fichier :

-   Miniature ou aperçu
-   Verbes spécifiques à une image dans le menu contextuel, par exemple :
    -   Faire pivoter l’aperçu
    -   Définir comme arrière-plan du Bureau
    -   Imprimer
-   Propriétés propres à l’image dans le volet d' **informations** , par exemple :
    -   Date de prise
    -   Balises
    -   Rating
-   Indexation du texte de fichier

Dans la capture d’écran suivante, le même fichier (désert. connu) a l’extension. jpg, qui est un type de fichier inscrit qui est associé à des gestionnaires de types de fichiers. ainsi, une image miniature et davantage de propriétés sont affichées.

![image avec un type de fichier inscrit et les gestionnaires de types de fichiers associés](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>Description du gestionnaire de types de fichiers

La fonctionnalité fournie par chaque gestionnaire de type de fichier est présentée dans le tableau suivant :



| Handler                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Menu contextuel](context-menu-handlers.md)                   | Un gestionnaire de menu contextuel, parfois appelé gestionnaire de menu contextuel, est un gestionnaire de type de fichier qui ajoute des commandes à un menu contextuel existant. Ces gestionnaires sont associés à un type de fichier particulier et sont appelés à chaque fois qu’un menu contextuel est affiché pour un membre du type de fichier.                                                                                                                                                                                                                                                                           |
| [Vidéo miniature](thumbnail-providers.md)                         | Gestionnaire qui fournit une image pour représenter un élément de Shell.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Propriété](../properties/building-property-handlers-properties.md) | Gestionnaire de propriétés qui fournit l’accès aux propriétés de l’élément pour Windows Search, l’Explorateur Windows et d’autres applications qui ont besoin d’accéder aux propriétés.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Préversion](preview-handlers.md)                              | Gestionnaire qui produit rapidement une vue simplifiée en lecture seule de l’élément à afficher dans le volet de visualisation de l’Explorateur Windows.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Filtres](../search/-search-3x-wds-extidx-filters.md)              | Un filtre, une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , qui analyse des documents pour le texte et les propriétés (également appelés attributs). Il extrait des segments de texte à partir de ces documents, en filtrant la mise en forme incorporée et en conservant les informations relatives à la position du texte. Il extrait également des blocs de valeurs, qui sont des propriétés d’un document entier ou de parties bien définies d’un document. **IFilter** fournit la base pour la création d’applications de niveau supérieur, telles que les indexeurs de documents et les visionneuses indépendantes des applications. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription de l’application](app-registration.md)
</dt> <dt>

[Types de fichiers](fa-file-types.md)
</dt> <dt>

[Fonctionnement des associations de fichiers](fa-how-work.md)
</dt> <dt>

[Affichage du contenu par type de fichier ou par type](prophand-content-view.md)
</dt> <dt>

[Vérificateur de type de fichier](file-type-verifier.md)
</dt> <dt>

[Identificateurs programmatiques](fa-progids.md)
</dt> <dt>

[Types perçus](fa-perceivedtypes.md)
</dt> <dt>

[Tableaux d’association](fa-associationarray.md)
</dt> </dl>

 

 
