---
description: Le vérificateur de type de fichier est un outil qui permet aux éditeurs de logiciels indépendants (ISV) de vérifier que leurs types de fichiers uniques sont correctement implémentés.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Vérificateur de type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad3d3e66d85413a209c6899ce16061fa1fd46468fa32462026485d49b7326dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009509"
---
# <a name="file-type-verifier"></a>Vérificateur de type de fichier

Le vérificateur de type de fichier est un outil qui permet aux éditeurs de logiciels indépendants (ISV) de vérifier que leurs types de fichiers uniques sont correctement implémentés. les implémentations de haute qualité de vos gestionnaires de types de fichiers sont cruciales pour une expérience utilisateur optimale, car les utilisateurs interagissent avec votre format de fichier de nombreuses façons dans Windows Explorer. Les utilisateurs peuvent effectuer des recherches en texte intégral, Trier par métadonnées personnalisées ou afficher des miniatures et des aperçus enrichis de votre format de fichier.

Pour obtenir des instructions sur l’utilisation du vérificateur de type de fichier, consultez la page [utilisation du vérificateur de type de fichier](how-to-use-the-file-type-verifier.md).

## <a name="about-the-file-type-verifier-tool"></a>À propos de l’outil de vérification de type de fichier

le vérificateur de Type de fichier est un programme qui est disponible dans le [kit de développement logiciel (SDK) Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx). il est conçu pour aider les développeurs qui créent des [types de fichiers](fa-file-types.md) Windows personnalisés à détecter les problèmes potentiels liés à leurs types de fichiers. bien que le vérificateur de type de fichier s’exécute uniquement sur Windows 7 et versions ultérieures, les règles appliquées par le vérificateur de type de fichier s’appliquent à toutes les versions de Windows où les fonctionnalités qu’il vérifie sont disponibles.

le vérificateur de type de fichier exécute plusieurs tests sur le type de fichier pour vérifier qu’il est correctement inscrit, et qu’il fournit les [gestionnaires de types de fichiers](fa-file-extensions.md) appropriés pour afficher correctement le type de fichier dans Windows Explorer et, le cas échéant, qu’il prend en charge l’indexation du contenu du fichier.

Le vérificateur de type de fichier teste les éléments suivants :

-   [Gestionnaires d’aperçus](building-preview-handlers.md)
-   [Gestionnaires de miniatures](building-thumbnail-providers.md)
-   [Gestionnaires de propriétés](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [Gestionnaires de verbes](fa-verbs.md)
-   [Filtres (IFilter)](../search/-search-3x-wds-extidx-filters.md)
-   [Associations de genres](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [Types perçus](fa-perceivedtypes.md)
-   [Propriétés importantes](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du vérificateur de type de fichier](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[Inscription de l’application](app-registration.md)
</dt> <dt>

[Types de fichiers](fa-file-types.md)
</dt> <dt>

[Fonctionnement des associations de fichiers](fa-how-work.md)
</dt> <dt>

[Affichage du contenu par type de fichier ou par type](prophand-content-view.md)
</dt> <dt>

[Gestionnaires de types de fichiers](fa-file-extensions.md)
</dt> <dt>

[Identificateurs programmatiques](fa-progids.md)
</dt> <dt>

[Types perçus](fa-perceivedtypes.md)
</dt> <dt>

[Tableaux d’association](fa-associationarray.md)
</dt> </dl>

 

 
