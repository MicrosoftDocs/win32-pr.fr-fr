---
description: Les propriétés sont extraites d’éléments à l’aide de gestionnaires de propriétés inscrits ou à l’aide de filtres inscrits pour des types de fichiers spécifiques. Un gestionnaire de filtres (implémentation de l’interface IFilter) peut interpréter le contenu d’un type de fichier de plusieurs façons.
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: Retour des propriétés d’un gestionnaire de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df0bfc811176e9b0672dbcbe4ef4f04f3c3a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514156"
---
# <a name="returning-properties-from-a-filter-handler"></a>Retour des propriétés d’un gestionnaire de filtres

Les propriétés sont extraites d’éléments à l’aide de gestionnaires de propriétés inscrits ou à l’aide de filtres inscrits pour des types de fichiers spécifiques. Un gestionnaire de filtres (implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) peut interpréter le contenu d’un type de fichier de plusieurs façons.

Cette rubrique est organisée comme suit :

- [Filtrage des propriétés](#returning-properties-from-a-filter-handler)
  - [Limitations de la taille des propriétés](#property-size-limitations)
- [Ressources supplémentaires](#additional-resources)
- [Rubriques connexes](#related-topics)

## <a name="property-filtering"></a>Filtrage des propriétés

Les meilleures pratiques pour le filtrage de propriétés sont répertoriées dans le tableau suivant.

| Méthode                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | Retourne l’énumération d' [**\_ indicateurs IFilter**](/windows/win32/api/filter/ne-filter-ifilter_flags) . Si le membre des *\_ \_ \_ propriétés OLE Flags IFilter* de cette énumération a la valeur 1, Windows Search utilise les interfaces des interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) et [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) pour énumérer et accéder aux propriétés de type valeur externe. |
| [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | Retourne des informations à partir d’un document dans des « segments » avec le type de bloc (texte ou valeur), le nom et les paramètres régionaux. Un segment contient une propriété de document.                                                                                                                                                                                                                                                                                                      |
| [**IFilter :: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | Obtient une propriété de type texte à partir d’un segment.                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | Obtient une propriété de type valeur à partir d’un segment.                                                                                                                                                                                                                                                                                                                                                                                                        |

L’illustration suivante montre un exemple de document. La propriété de type valeur externe `DocTitle` (obtenue à l’aide de méthodes des interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) et [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) ) et la propriété de type valeur interne `Book` (obtenue à la suite d’une implémentation [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) personnalisée) décrivent le document dans son ensemble. Les propriétés de type texte `Contents` et `Chapter` décrivent le contenu du document. Lors du traitement de ce document, le gestionnaire de filtre (une implémentation de l’interface **IFilter** ) identifie et extrait ces propriétés.

![Diagramme montrant les éléments d’un document standard](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>Limitations de la taille des propriétés

Il existe deux limitations potentielles à la taille des propriétés :

- Taille maximale des données que Windows Search accepte par fichier.
- Taille maximale par propriété telle que définie dans le fichier de description de la propriété.

Actuellement, Windows Search n’utilise pas la taille de propriété définie lors du calcul de la quantité de données qu’il accepte à partir d’un élément. Au lieu de cela, la limite d’utilisation de la recherche Windows est le produit de la taille du fichier et le `MaxGrowFactor` (taille de fichier N \* MaxGrowFactor) lu à partir du Registre. La valeur par défaut `MaxGrowFactor` est quatre.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

Par conséquent, si la taille totale de votre type de fichier est faible, mais que les propriétés sont plus volumineuses, la recherche Windows peut ne pas accepter toutes les données de propriété que vous souhaitez émettre. Toutefois, vous pouvez augmenter le `MaxGrowFactor` en fonction de vos besoins.

## <a name="additional-resources"></a>Ressources supplémentaires

- L’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), montre comment créer une classe de base IFilter pour l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
- Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).
- Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
- Pour obtenir une vue d’ensemble des propriétés et des gestionnaires de propriétés, ainsi qu’une liste des propriétés système que vous pouvez utiliser pour vos formats de fichier, consultez [développement de gestionnaires de propriétés pour Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="related-topics"></a>Rubriques connexes

[Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)

[À propos des gestionnaires de filtres dans Windows Search](-search-ifilter-about.md)

[Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md)

[Gestionnaires de filtres fournis avec Windows](-search-ifilter-implementations.md)

[Implémentation de gestionnaires de filtres dans Windows Search](-search-ifilter-constructing-filters.md)

[Inscription des gestionnaires de filtres](-search-ifilter-registering-filters.md)

[Test des gestionnaires de filtres](-search-ifilter-testing-filters.md)
