---
description: découvrez comment développer des gestionnaires de filtres dans Windows recherche. La recherche utilise des filtres pour extraire les éléments à inclure dans un index de recherche en texte intégral.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: développement de gestionnaires de filtres pour la recherche de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cb8fe61ce85c86d0b8397d81303014ed1268bc0aef96b22e7b7bab335b7f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597819"
---
# <a name="developing-filter-handlers-for-windows-search"></a>développement de gestionnaires de filtres pour la recherche de Windows

Microsoft Windows Search utilise des filtres pour extraire le contenu des éléments à inclure dans un index de recherche en texte intégral. vous pouvez étendre Windows recherche pour indexer les types de fichiers nouveaux ou propriétaires en écrivant des filtres pour extraire le contenu et les gestionnaires de propriétés pour extraire les propriétés des fichiers.

Cette section fournit l’infrastructure conceptuelle nécessaire à l’implémentation d’un gestionnaire de filtres (une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).

- [fonctionnement des gestionnaires de filtres dans la recherche Windows](-search-ifilter-about.md)
- [meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md)
- [Retour des propriétés d’un gestionnaire de filtres](-search-ifilter-property-filtering.md)
- [Gestionnaires de filtres fournis avec Windows](-search-ifilter-implementations.md)
- [implémentation de gestionnaires de filtres dans Windows Search](-search-ifilter-constructing-filters.md)
- [Inscription des gestionnaires de filtres](-search-ifilter-registering-filters.md)
- [Test des gestionnaires de filtres](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>Ressources supplémentaires

- l’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), illustre la création d’une classe de base ifilter pour l’implémentation de l’interface [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
- Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).
- Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).
