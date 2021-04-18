---
description: Vous pouvez étendre Windows Search pour indexer le contenu et les propriétés de nouveaux formats de fichier, ainsi que les magasins de données à l’aide d’interfaces de complément de données.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Extension de l’index (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512943"
---
# <a name="extending-the-index-windows-search"></a>Extension de l’index (Windows Search)

Vous pouvez étendre Windows Search pour indexer le contenu et les propriétés de nouveaux formats de fichier, ainsi que les magasins de données à l’aide d' [interfaces de complément de données](./-search-data-addins-interfaces-entry-page.md). Pour créer des compléments de recherche Windows, les développeurs tiers doivent tout d’abord implémenter un magasin de données Shell, puis développer un gestionnaire de protocole pour que la recherche Windows puisse accéder aux données pour l’indexation. Si vous disposez d’un format de fichier personnalisé, vous devez développer un gestionnaire de filtre pour indexer le contenu du fichier et un gestionnaire de propriétés pour chaque type de fichier aux propriétés d’index.

Windows Search prend actuellement en charge l’indexation de plus de 200 types d’éléments (tels que les formats de fichier. txt,. html et. Xml) et peut fonctionner avec plusieurs types de magasins de données (tels que le système de fichiers NTFS et Microsoft Outlook). Windows Search utilise une technologie de filtre et de gestionnaire de protocole similaire à celle de SharePoint Server. Par conséquent, si vous avez déjà des implémentations pour votre format de fichier, vous pouvez mettre à jour les implémentations à initialiser avec un flux à l’aide de [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) afin que le filtre fonctionne avec la recherche Windows.

> [!Note]  
> Les gestionnaires de filtres, les gestionnaires de propriétés et les gestionnaires de protocole doivent être écrits en code natif. Cela est dû à des problèmes potentiels de contrôle de version du common language runtime (CLR) avec le processus dans lequel plusieurs compléments s’exécutent.

 

Cette section sur l’extension de l’index avec les compléments contient les rubriques suivantes :

-   [Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)
-   [Développement de gestionnaires de propriétés pour Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
-   [Développement de gestionnaires de protocole](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a>Ressources supplémentaires

Pour obtenir des exemples de code associés, consultez [exemples de code Windows Search](-search-samples-ovw.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de développement de Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Gestion de l’index](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Interrogation de l’index programmatiquement](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Extension des ressources linguistiques](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
