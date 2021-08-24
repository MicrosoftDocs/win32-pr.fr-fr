---
description: Les propriétés sont extraites d’éléments à l’aide de gestionnaires de propriétés inscrits ou à l’aide de filtres inscrits pour des types de fichiers spécifiques. Un gestionnaire de filtres (implémentation de l’interface IFilter) peut interpréter le contenu d’un type de fichier de plusieurs façons.
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: Retour des propriétés d’un gestionnaire de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1842710af65e22f5a730891ea6e7f32053b92212f8c3ad4c5f0f68f23578d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594852"
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
| [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | Retourne l’énumération d' [**\_ indicateurs IFilter**](/windows/win32/api/filter/ne-filter-ifilter_flags) . si le membre des *\_ \_ \_ propriétés OLE flags IFILTER* de cette énumération a la valeur 1, Windows recherche utilise les interfaces d’interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) et [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) pour énumérer et accéder aux propriétés de type valeur externe. |
| [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | Retourne des informations à partir d’un document dans des « segments » avec le type de bloc (texte ou valeur), le nom et les paramètres régionaux. Un segment contient une propriété de document.                                                                                                                                                                                                                                                                                                      |
| [**IFilter :: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | Obtient une propriété de type texte à partir d’un segment.                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | Obtient une propriété de type valeur à partir d’un segment.                                                                                                                                                                                                                                                                                                                                                                                                        |

L’illustration suivante montre un exemple de document. La propriété de type valeur externe `DocTitle` (obtenue à l’aide de méthodes des interfaces [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) et [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) ) et la propriété de type valeur interne `Book` (obtenue à la suite d’une implémentation [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) personnalisée) décrivent le document dans son ensemble. Les propriétés de type texte `Contents` et `Chapter` décrivent le contenu du document. Lors du traitement de ce document, le gestionnaire de filtre (une implémentation de l’interface **IFilter** ) identifie et extrait ces propriétés.

![Diagramme montrant les éléments d’un document standard](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>Limitations de la taille des propriétés

Il existe deux limitations potentielles à la taille des propriétés :

- taille maximale des données que Windows recherche accepte par fichier.
- Taille maximale par propriété telle que définie dans le fichier de description de la propriété.

actuellement, Windows Search n’utilise pas la taille de propriété définie lors du calcul de la quantité de données qu’il accepte à partir d’un élément. au lieu de cela, la limite Windows utilisée par la recherche est le produit de la taille du fichier et le `MaxGrowFactor` (taille de fichier N \* MaxGrowFactor) lu à partir du registre. La valeur par défaut `MaxGrowFactor` est quatre.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

par conséquent, si la taille totale de votre type de fichier est faible, mais que les propriétés sont plus volumineuses, Windows recherche peut ne pas accepter toutes les données de propriété que vous souhaitez émettre. Toutefois, vous pouvez augmenter le `MaxGrowFactor` en fonction de vos besoins.

## <a name="additional-resources"></a>Ressources supplémentaires

- l’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), illustre la création d’une classe de base ifilter pour l’implémentation de l’interface [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
- Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).
- Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
- pour obtenir une vue d’ensemble des propriétés et des gestionnaires de propriétés, ainsi qu’une liste des propriétés système que vous pouvez utiliser pour vos formats de fichier, consultez [développement de gestionnaires de propriétés pour la recherche de Windows](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="related-topics"></a>Rubriques connexes

[Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)

[à propos des gestionnaires de filtres dans Windows Search](-search-ifilter-about.md)

[meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md)

[Gestionnaires de filtres fournis avec Windows](-search-ifilter-implementations.md)

[implémentation de gestionnaires de filtres dans Windows Search](-search-ifilter-constructing-filters.md)

[Inscription des gestionnaires de filtres](-search-ifilter-registering-filters.md)

[Test des gestionnaires de filtres](-search-ifilter-testing-filters.md)
