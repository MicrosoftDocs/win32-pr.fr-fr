---
description: Cette rubrique décrit une nouvelle vue dans l’Explorateur Windows, appelée affichage du contenu, qui affiche le contenu le plus pertinent pour chaque élément.
title: Affichage du contenu par type de fichier ou par type
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757360"
---
# <a name="content-view-by-file-type-or-kind"></a>Affichage du contenu par type de fichier ou par type

Cette rubrique décrit une nouvelle vue dans l’Explorateur Windows, appelée affichage du contenu, qui affiche le contenu le plus pertinent pour chaque élément. À l’aide d’un ensemble de clés de Registre, les éléments peuvent définir une liste de propriétés et une disposition que l’interpréteur de commandes utilise pour la vue de contenu. L’interpréteur de commandes récupère les clés de Registre à l’aide du [tableau d’association](fa-perceivedtypes.md)de l’élément.

## <a name="how-does-the-content-view-work"></a>Comment fonctionne l’affichage du contenu ?

Dans Windows 7 et versions ultérieures, l’affichage du contenu utilise une logique de redimensionnement qui supprime les propriétés lorsque la taille de la fenêtre diminue, pour s’assurer que les propriétés les plus critiques ont encore de la place pour être clairement lisibles. La capture d’écran suivante illustre l’affichage du contenu des résultats de recherche contenant de la musique, des images et des documents.

![affichage du contenu des résultats de la recherche contenant de la musique, des images et des documents](images/content-view/contentviewsearchresults.png)

Certaines sources de données de l’interpréteur de commandes utilisent l’affichage du contenu par défaut, mais les utilisateurs peuvent sélectionner l’affichage du contenu en cliquant sur le bouton **afficher le contrôle** dans l’Explorateur Windows. Une source de données Shell étend l’espace de noms Shell et expose des éléments dans un magasin de données. Les éléments d’un magasin de données peuvent être indexés par le système de recherche Windows à l’aide d’un gestionnaire de protocole.

## <a name="how-to-implement-the-content-view"></a>Comment implémenter l’affichage du contenu

Lors de l’inscription d’un nouveau [type de fichier](fa-file-types.md) ou [Gestionnaire de protocole](../search/-search-3x-wds-extidx-prot-implementing.md), vous pouvez tirer parti de l’affichage de contenu à l’aide de l’une des deux approches. Vous pouvez utiliser un ensemble de propriétés et un modèle de disposition existants, ou vous pouvez créer votre propre combinaison.

Vous pouvez utiliser une entrée de Registre pour associer votre type de fichier ou élément à un [type](../properties/building-property-handlers-user-friendly-kind-names.md)prédéfini, qui est une propriété que vous pouvez considérer comme une catégorie de contenu. En associant votre type de fichier ou élément à certains de ces genres, vous héritez automatiquement des modèles de disposition de vue de contenu et des listes de propriétés de ce type. Windows définit les modèles de disposition de vue de contenu et les listes de propriétés pour les types suivants : documents, courrier électronique, dossier, musique, image et générique. Ce type d’association est encouragé. Elle vous permet de fournir une expérience cohérente qu’un utilisateur attend pour des éléments similaires.

Pour plus d’informations, consultez [types de fichiers](fa-file-types.md) et [noms](../properties/building-property-handlers-user-friendly-kind-names.md) de types et [comment inscrire un ensemble de propriétés d’affichage de contenu unique et un modèle de disposition pour le type de fichier ou l’élément](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour obtenir une documentation de référence sur les propriétés, consultez [System. Kind](../properties/props-system-kind.md)et [System. KindText](../properties/props-system-kindtext.md).
-   Pour obtenir une documentation de référence PropList, consultez [System. PropList. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)et [System. PropList. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription de l’application](app-registration.md)
</dt> <dt>

[Types de fichiers](fa-file-types.md)
</dt> <dt>

[Fonctionnement des associations de fichiers](fa-how-work.md)
</dt> <dt>

[Vérificateur de type de fichier](file-type-verifier.md)
</dt> <dt>

[Gestionnaires de types de fichiers](fa-file-extensions.md)
</dt> <dt>

[Identificateurs programmatiques](fa-progids.md)
</dt> <dt>

[Types perçus](fa-perceivedtypes.md)
</dt> <dt>

[Tableaux d’association](fa-associationarray.md)
</dt> </dl>

 

 
