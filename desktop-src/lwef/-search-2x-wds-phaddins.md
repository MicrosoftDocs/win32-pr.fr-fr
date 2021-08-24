---
title: Développement de compléments de gestionnaires de protocole
description: vous pouvez étendre Microsoft Windows Desktop Search (WDS) pour inclure de nouveaux magasins de données en implémentant un gestionnaire de protocole personnalisé.
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc107c8ca51d43e2602206eb993cea6cac6dd9ec866670235daf7fb81452f5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726499"
---
# <a name="developing-protocol-handler-add-ins"></a>Développement de compléments de gestionnaires de protocole

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

vous pouvez étendre Microsoft Windows Desktop Search (WDS) pour inclure de nouveaux magasins de données en implémentant un gestionnaire de protocole personnalisé.

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indexation des magasins de données à l’aide de gestionnaires de protocole

Un magasin de données est une source de contenu (système de base de données, répertoire, système de fichiers) dans laquelle les données sont stockées et peuvent être analysées par l’indexeur WDS. Le magasin peut être hiérarchique (comme une base de données) ou basé sur des liens (comme un site Web). Un gestionnaire de protocole permet d’indexer des applications telles que WDS pour analyser systématiquement les nœuds d’un magasin de données afin d’extraire les informations pertinentes à inclure dans l’index. Chaque gestionnaire de protocole est utilisé pour indexer un type spécifique de magasin de données. WDS est livré avec des gestionnaires de protocole pour les magasins de système de fichiers et pour les banques de données microsoft Outlook et microsoft Outlook Express (magasins de courrier électronique,. Fichiers PST, etc.). lors de l’indexation Outlook courrier électronique, par exemple, le gestionnaire de protocole analyse tous les messages de tous les dossiers en extrayant les informations de chaque message et pièce jointe. Ces informations sont transmises à l’indexeur à inclure dans le catalogue WDS.

Souvent, les utilisateurs doivent effectuer des recherches dans d’autres magasins de données, tels que les bases de données héritées, les magasins de messagerie ou les structures de données non pris en charge par WDS. Vous pouvez étendre WDS pour analyser un nouveau magasin de données à l’aide de ou de l’implémentation d’un gestionnaire de protocole spécifiquement pour ce magasin de données. Tout d’abord, vous devez déterminer si un gestionnaire de protocole existe déjà pour votre magasin de données, peut-être pour une utilisation avec une autre application comme SharePoint Services. Dans ce cas, vous pouvez installer ce gestionnaire de protocole sur le système. Toutefois, si un autre gestionnaire de protocole n’existe pas, vous devez en implémenter un. les gestionnaires de protocole WDS utilisent les mêmes spécifications de conception que SharePoint Services, et ils peuvent souvent être utilisés de manière interchangeable.

En outre, si le magasin de données contient des données ou des types de fichier autres que l’un des types de fichiers 200 pris en charge par WDS, vous devez également implémenter un filtre pour accéder au contenu des éléments du magasin et l’indexer. WDS 2. x utilise le gestionnaire de protocole et la technologie [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)utilisés par SharePoint Services. Si vous avez déjà des filtres pour un magasin et un type de fichier spécifiques installés sur le système en cours d’indexation, WDS utilise les interfaces existantes pour indexer ces données.

 

## <a name="roadmap-to-adding-new-data-stores"></a>Feuille de route pour l’ajout de nouveaux magasins de données

Pour étendre WDS en vue d’analyser de nouveaux magasins de données, vous pouvez créer un gestionnaire de protocole et un ou plusieurs des compléments suivants : gestionnaire de menu contextuel, gestionnaire d’icône et complément SearchProtocolOptions.

1.  Créez et inscrivez un gestionnaire de protocole multithread pour le magasin de données :
    -   **ISearchProtocol** : cette interface accède à un protocole et mappe une URL à un IUrlAccessor.
    -   **IUrlAccessor** : il s’agit de l’interface principale utilisée pour accéder aux éléments à partir de la source de contenu et lier le contenu au filtre approprié.
    -   **IProtocolHandlerSite** : cette interface permet de demander et de charger des filtres supplémentaires.
    -   **IFilter** : cette interface retourne l’URL de chaque élément d’un dossier en tant que propriétés de valeur pour le traitement.

    > [!Note]
    >
    > La fonctionnalité de complément minimale nécessaire pour retourner les résultats de recherche à partir d’un magasin de données non hiérarchique est une implémentation d’interfaces ISearchProtocol et IUrlAccessor.

     

2.  Implémentez l’interface ISearchProtocolOptions pour inclure des options de gestionnaire de protocole personnalisées, telles que des pages de démarrage prédéfinies :
    -   **ISearchProtocolOptions** : cette interface définit les URL par défaut que le gestionnaire de protocole doit traiter, détermine la configuration requise pour un gestionnaire de protocole et détermine si les spécifications ont été satisfaites sur un système donné.
3.  Étendez l’interpréteur de commandes pour inclure des éléments d’interface utilisateur, tels que des menus contextuels et des icônes spécifiques aux fichiers, en implémentant les interfaces suivantes :
    -   **IShellFolder** : cette interface, qui est utilisée pour gérer les dossiers, est requise pour fournir les interfaces IContextMenu et IExtractIcon pour une URL dans un nouveau magasin.
    -   **IPersistFolder** : cette interface est requise pour indiquer à un objet de dossier de Shell de s’initialiser.
    -   **IPersist** : cette interface fournit l’identificateur de classe (CLSID) d’un objet qui peut être stocké de manière permanente dans le système.
    -   **IContextMenu** : cette interface définit le menu contextuel d’un élément désigné par une URL.
    -   **IExtractIcon** : cette interface définit l’icône à afficher pour un élément désigné par une URL.
4.  Implémentez un mécanisme pour notifier l’indexeur des modifications à votre banque de données :
    -   **ISearchItemsChangedSink** : cette interface permet à votre gestionnaire de protocole de notifier l’index des modifications apportées à votre magasin de données. Cela améliore les performances en garantissant que l’indexeur n’analyse pas l’intégralité du magasin sur les index incrémentiels.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Implémentation d’un gestionnaire de protocole pour WDS](-search-2x-wds-phimplementing.md)
</dt> <dt>

[Ajout d’icônes, d’aperçus et de menus contextuels avec des extensions de Shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Notification de l’index des modifications](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Installation et inscription de gestionnaires de protocole](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 