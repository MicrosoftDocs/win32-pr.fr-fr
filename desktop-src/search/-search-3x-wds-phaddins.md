---
description: Cette section fournit des informations conceptuelles nécessaires à l’implémentation, l’extension et le test des gestionnaires de protocole.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: Développement de gestionnaires de protocole pour Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e56c237dd4876ae05bcd7b983c4da2708f299a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750428"
---
# <a name="developing-protocol-handlers-for-windows-search"></a>Développement de gestionnaires de protocole pour Windows Search

Cette section fournit des informations conceptuelles nécessaires à l’implémentation, l’extension et le test des gestionnaires de protocole.

-   [Fonctionnement des gestionnaires de protocole](-search-3x-wds-extidx-prot-implementing.md)
-   [Notification de l’index des modifications](-search-3x-wds-notifyingofchanges.md)
-   [Ajout d’icônes et de menus contextuels](-search-3x-wds-ph-ui-extensions.md)
-   [Exemple de code : extensions de Shell pour les gestionnaires de protocole](-search-3x-wds-ph-ui-samplecode.md)
-   [Installation et inscription de gestionnaires de protocole](-search-3x-wds-ph-install-registration.md)
-   [Création d’un connecteur de recherche pour un gestionnaire de protocole](-search-3x-wds-ph-search-connector.md)
-   [Débogage de gestionnaires de protocole](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a>Ressources supplémentaires

Pour obtenir des informations conceptuelles sur l’indexation, consultez les rubriques suivantes :

-   Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
-   Pour étendre Windows Search afin d’indexer le contenu et les propriétés de nouveaux formats de fichier et de magasins de données, consultez [extension de l’index](-search-3x-wds-extidx-overview.md).
-   Pour obtenir une vue d’ensemble du gestionnaire de catalogues et du gestionnaire de recherche de catalogue (CSM), consultez [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md) et [utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md).

Pour obtenir des informations conceptuelles conceptuelles sur les types de fichiers et les gestionnaires, consultez les rubriques suivantes :

-   Pour étendre l’interpréteur de commandes avec des gestionnaires de types de fichiers, consultez [création de gestionnaires d’extension de Shell](../shell/handlers.md).
-   Pour obtenir des informations conceptuelles sur les gestionnaires de filtres, consultez [développement de gestionnaires de filtres](-search-ifilter-conceptual.md).
-   Pour plus d’informations sur la création de gestionnaires, consultez [Introduction aux associations de fichiers](../shell/fa-intro.md), [inscription d’extensions de Shell](../shell/reg-shell-exts.md), création de gestionnaires d’extensions de [Shell](../shell/handlers.md), [menu contextuel](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))et [gestionnaires d’aperçus](../shell/preview-handlers.md).

Pour plus d’informations sur les technologies associées et sur l’implémentation d’un magasin de données, consultez les rubriques suivantes :

-   Les gestionnaires de protocoles de recherche Windows utilisent des spécifications de conception similaires à celles de SharePoint Server, et ils peuvent souvent être utilisés de manière interchangeable. Pour plus d’informations, consultez le [Centre de développement SharePoint Server](https://developer.microsoft.com/office/docs).
-   Dans Windows 7 et versions ultérieures, SharePoint Search Server 2008 et MOSS 2007 SP2 prennent également en charge la recherche fédérée. Pour plus d’informations sur le déploiement de la recherche fédérée et du serveur de recherche 2008 avec Office SharePoint Server 2007, voir serveur de recherche de recherche [fédéré \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)).
-   Pour créer un magasin de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Pour obtenir des exemples de code, consultez les pages suivantes du portail :

-   Pour obtenir des exemples de code de recherche, consultez les [exemples du kit de développement Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).
-   Pour obtenir des exemples de code Shell, consultez [Shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).

 

 
