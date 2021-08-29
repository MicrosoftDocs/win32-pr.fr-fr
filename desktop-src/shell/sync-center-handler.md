---
description: Cette rubrique fournit un examen pas à pas de la configuration requise pour créer un fichier DLL qui implémente un gestionnaire à utiliser avec le centre de synchronisation. ces informations sont valides à partir de Windows Vista.
title: développement d’un gestionnaire de Windows Sync Center
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 66b40f81-9515-4190-8ced-44f20bb9df86
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 127426365ff0f2c7bbada34f87cc7e2aec8916a2dbe4038978835aa61b179cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967908"
---
# <a name="developing-a-windows-sync-center-handler"></a>développement d’un gestionnaire de Windows Sync Center

Cette rubrique fournit un examen pas à pas de la configuration requise pour créer un fichier DLL qui implémente un gestionnaire à utiliser avec le centre de synchronisation. ces informations sont valides à partir de Windows Vista.

-   [l’expérience de synchronisation Windows avant Vista](#the-windows-synchronization-experience-before-vista)
-   [API du centre de synchronisation](#sync-center-apis)
    -   [Interfaces essentielles](#essential-interfaces)

## <a name="the-windows-synchronization-experience-before-vista"></a>l’expérience de synchronisation Windows avant Vista

Windows XP a fourni un [Gestionnaire de synchronisation](syncmgr-start-page.md) (mobsync.exe). De nombreux appareils, tels que les lecteurs MP3, les téléphones cellulaires et les appareils photo, ont également fourni leurs propres interfaces de synchronisation plutôt que d’utiliser le gestionnaire de synchronisation. Cela a abouti à une expérience utilisateur incohérente et non centralisée.

la nouvelle fonctionnalité du centre de synchronisation fournie dans Windows Vista présente plusieurs avantages par rapport à l’ancien gestionnaire de synchronisation.

-   Meilleure détectabilité
-   Moins besoin d’une action directe de l’utilisateur
-   Ne bloque pas les autres opérations
-   Meilleure visualisation de la progression de la synchronisation
-   Modèle de développement plus facile à comprendre

## <a name="sync-center-apis"></a>API du centre de synchronisation

Le centre de synchronisation communique avec les gestionnaires via un certain nombre d’interfaces COM (Component Object Model). Toutes ces interfaces ne sont pas nécessaires pour implémenter un gestionnaire du centre de synchronisation. Cette rubrique a été divisée en deux sections. La première section explique les interfaces COM essentielles que chaque gestionnaire doit prendre en charge, et la deuxième section examine les interfaces COM facultatives et examine les raisons pour lesquelles un gestionnaire les prend en charge.

-   [Interfaces essentielles](#essential-interfaces)

### <a name="essential-interfaces"></a>Interfaces essentielles

Tous les gestionnaires du centre de synchronisation doivent prendre en charge les interfaces suivantes :

-   [**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler)
-   [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo)
-   [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer)
-   [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems)
-   [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem)
-   [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo)

[**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) et [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) sont utilisés pour décrire un élément de synchronisation unique impliqué dans la synchronisation dans le centre de synchronisation. Un élément de synchronisation représente généralement un type de données particulier (tel que des images) ou un emplacement de données particulier.

Les éléments de synchronisation qui représentent des emplacements de données différents permettent des synchronisations très spécifiques. La granularité de l’emplacement est jusqu’à l’auteur du gestionnaire, mais il est important de le faire dans la conception. Si le nombre d’éléments de synchronisation (emplacements) est trop faible, l’utilisateur est limité dans la mesure où il ne peut synchroniser que certaines données. À l’autre extrême, une granularité trop importante peut devenir ingérable.

Si un gestionnaire prend en charge plusieurs types de données ou plusieurs emplacements de données, il doit prendre en charge plusieurs objets d’élément de synchronisation. Il peut s’agir, par exemple, d’un assistant de données personnelles (PDA) qui permet à l’utilisateur de synchroniser des contacts, des éléments de calendrier et des documents. Ces trois types de données doivent être représentés par trois objets uniques qui exposent chacun les interfaces [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) et [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) .

L’interface [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems) fournit un mécanisme pour énumérer les éléments de synchronisation d’un gestionnaire. Pour récupérer cet énumérateur, le centre de synchronisation appelle la méthode [**ISyncMgrSyncItemContainer :: GetSyncItemEnumerator**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator) exposée par le gestionnaire. [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer) contient également deux autres méthodes que le centre de synchronisation peut utiliser pour récupérer des informations sur les éléments de synchronisation du gestionnaire :

-   [**GetSyncItem**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem) retourne un élément de synchronisation spécifique.
-   [**GetSyncItemCount**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount) retourne le nombre d’éléments de synchronisation pris en charge par le gestionnaire.

[**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler) et [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo) sont utilisés pour décrire les propriétés du gestionnaire de la main et lancer la synchronisation réelle. [**ISyncMgrHandler :: Synchronize**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandler-synchronize) est l’endroit où le code du gestionnaire effectue la synchronisation et fournit des commentaires sur la progression et les problèmes qui se produisent.

La plupart des méthodes d’interface n’ont pas besoin d’être entièrement implémentées. Le centre de synchronisation fournit une certaine quantité d’informations par défaut. Les interfaces permettent à un gestionnaire de remplacer ces informations et de fournir des informations personnalisées à afficher, si nécessaire.

 

 



