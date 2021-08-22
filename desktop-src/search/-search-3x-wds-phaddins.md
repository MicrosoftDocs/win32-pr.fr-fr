---
description: Cette section fournit des informations conceptuelles nécessaires à l’implémentation, l’extension et le test des gestionnaires de protocole.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: développement de gestionnaires de protocole pour la recherche de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ef01d36e565471756ee9d6680833401054a6e29b9c570dad7852d316797067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597829"
---
# <a name="developing-protocol-handlers-for-windows-search"></a>développement de gestionnaires de protocole pour la recherche de Windows

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
-   pour étendre Windows recherche afin d’indexer le contenu et les propriétés de nouveaux formats de fichier et de banques de données, consultez [extension de l’index](-search-3x-wds-extidx-overview.md).
-   Pour obtenir une vue d’ensemble du gestionnaire de catalogues et du gestionnaire de recherche de catalogue (CSM), consultez [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md) et [utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md).

Pour obtenir des informations conceptuelles conceptuelles sur les types de fichiers et les gestionnaires, consultez les rubriques suivantes :

-   Pour étendre l’interpréteur de commandes avec des gestionnaires de types de fichiers, consultez [création de gestionnaires d’extension de Shell](../shell/handlers.md).
-   Pour obtenir des informations conceptuelles sur les gestionnaires de filtres, consultez [développement de gestionnaires de filtres](-search-ifilter-conceptual.md).
-   Pour plus d’informations sur la création de gestionnaires, consultez [Introduction aux associations de fichiers](../shell/fa-intro.md), [inscription d’extensions de Shell](../shell/reg-shell-exts.md), création de gestionnaires d’extensions de [Shell](../shell/handlers.md), [menu contextuel](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))et [gestionnaires d’aperçus](../shell/preview-handlers.md).

Pour plus d’informations sur les technologies associées et sur l’implémentation d’un magasin de données, consultez les rubriques suivantes :

-   Windows les gestionnaires de protocoles de recherche utilisent des spécifications de conception similaires à SharePoint Server et peuvent souvent être utilisés de manière interchangeable. pour plus d’informations, consultez [SharePoint Server developer Center](https://developer.microsoft.com/office/docs).
-   dans Windows 7 et versions ultérieures, SharePoint search Server 2008 et MOSS 2007 SP2 prennent également en charge la recherche fédérée. pour plus d’informations sur le déploiement de la recherche fédérée et du serveur de recherche 2008 avec Office SharePoint server 2007, voir serveur de recherche fédéré de recherche [ \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)).
-   Pour créer un magasin de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Pour obtenir des exemples de code, consultez les pages suivantes du portail :

-   pour obtenir des exemples de code de recherche, consultez [Windows les exemples du kit de développement logiciel (SDK)](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).
-   Pour obtenir des exemples de code Shell, consultez [Shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).

 

 
