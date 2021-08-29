---
description: vous pouvez étendre Windows recherche pour indexer le contenu et les propriétés de nouveaux formats de fichier, ainsi que les magasins de données à l’aide d’interfaces de complément de données.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Extension de l’index (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6faa3ab6ba7631840bcc324bbd163c9e182c611be7e94c6a856e9949ca6857e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597879"
---
# <a name="extending-the-index-windows-search"></a>Extension de l’index (Windows Search)

vous pouvez étendre Windows recherche pour indexer le contenu et les propriétés de nouveaux formats de fichier, ainsi que les magasins de données à l’aide d' [interfaces de complément de données](./-search-data-addins-interfaces-entry-page.md). pour créer Windows compléments de recherche, les développeurs tiers doivent tout d’abord implémenter un magasin de données Shell, puis développer un gestionnaire de protocole afin que Windows recherche puisse accéder aux données pour l’indexation. Si vous disposez d’un format de fichier personnalisé, vous devez développer un gestionnaire de filtre pour indexer le contenu du fichier et un gestionnaire de propriétés pour chaque type de fichier aux propriétés d’index.

Windows La recherche prend actuellement en charge l’indexation de plus de 200 types d’éléments (tels que les formats de fichiers .txt, .html et .xml) et peut fonctionner avec plusieurs types de magasins de données (tels que le système de fichiers NTFS et Microsoft Outlook). Windows la recherche utilise une technologie de filtre et de gestionnaire de protocole similaire à SharePoint Server. par conséquent, si vous avez déjà des implémentations pour votre format de fichier, vous pouvez mettre à jour les implémentations à initialiser avec un flux à l’aide de [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) afin que le filtre fonctionne avec Windows recherche.

> [!Note]  
> Les gestionnaires de filtres, les gestionnaires de propriétés et les gestionnaires de protocole doivent être écrits en code natif. Cela est dû à des problèmes potentiels de contrôle de version du common language runtime (CLR) avec le processus dans lequel plusieurs compléments s’exécutent.

 

Cette section sur l’extension de l’index avec les compléments contient les rubriques suivantes :

-   [Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)
-   [développement de gestionnaires de propriétés pour la recherche de Windows](-search-3x-wds-extidx-propertyhandlers.md)
-   [Développement de gestionnaires de protocole](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a>Ressources supplémentaires

pour obtenir des exemples de code associés, consultez [Windows des exemples de code de recherche](-search-samples-ovw.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Rechercher dans le Guide de développement](-search-developers-guide-entry-page.md)
</dt> <dt>

[Gestion de l’index](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Interrogation de l’index programmatiquement](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Extension des ressources linguistiques](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
