---
description: L’interface ISearchManager fournit des méthodes qui effectuent des modifications dans les catalogues.
ms.assetid: e6f4432b-03bf-4711-a79e-1bf9242c5683
title: Utilisation du gestionnaire de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e8c52211c7d69ba7a50c9a9925dad8bb84f848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951037"
---
# <a name="using-the-search-manager"></a>Utilisation du gestionnaire de recherche

L’interface [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) fournit des méthodes qui effectuent des modifications dans les catalogues. Les modifications apportées au niveau **ISearchManager** s’appliquent globalement à tous les catalogues utilisés par l’indexeur, tandis que les modifications apportées au niveau du [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) s’appliquent à des catalogues spécifiques. Toutefois, actuellement, Windows Search n’utilise qu’un seul catalogue, SystemIndex. Vous pouvez utiliser le gestionnaire de recherche pour effectuer les opérations suivantes :

- Obtient une instance du gestionnaire de catalogues pour le catalogue de recherche.
- Obtenir des informations sur la version du moteur de recherche Windows.

Les méthodes suivantes de l’interface [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) peuvent vous aider à gérer vos catalogues de recherche :

| Méthode                                                                      | Description                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCatalog,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)                     | Obtient un catalogue par nom et retourne une instance de [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) pour ce catalogue. Cela vous permet de gérer un catalogue de recherche individuel.                                          |
| [**GetIndexerVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversion)       | Retourne la version de l’indexeur en deux entiers : version principale et version mineure. Par exemple, le numéro de version principale pour Windows 10 Search est « 10 » et le numéro de version secondaire est « 0 ». Pour Windows Vista Search et Windows Search 3,0 sur Windows XP, le numéro de version principale est « 3 » et le numéro de version secondaire est « 0 ». |
| [**GetIndexerVersionStr**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversionstr) | Retourne le numéro de version complet de l’indexeur sous la forme d’une chaîne : par exemple, « 10.0.18309.1000 ». Pour Windows 10, cela correspond généralement au numéro de version du système d’exploitation. Pour Windows XP, Vista et 7, il sera différent.                                                                                                                                        |


Pour plus d’informations sur ces méthodes, consultez la documentation [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .

Les méthodes [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) suivantes sont réservées pour une utilisation ultérieure. Toutefois, elles sont implémentées et n’affectent pas l’indexeur ou le catalogue, car il n’existe qu’un seul catalogue pour Windows Search pour l’instant.

- **accéder à \_ BypassList**
- **Obtient \_ LocalBypass**
- **recevoir le \_ numéro_port**
- **Obtient \_ ProxyName**
- **Obtient \_ UseProxy**
- **demander à \_ UserAgent**
- **placer \_ UserAgent**
- **SetProxy**

**GetParameter** et **SetParameter** sont également réservés pour une utilisation ultérieure, mais ils ne sont pas implémentés.

## <a name="related-topics"></a>Rubriques connexes

[Gestion de l’index](-search-3x-wds-mngidx-overview.md)

[Interfaces pour la gestion de l’index](interfaces-for-managing-the-index.md)

[Utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md)

[Utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md)
