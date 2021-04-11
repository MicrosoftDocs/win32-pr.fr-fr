---
description: Cette rubrique décrit les technologies liées à la recherche Windows.
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: Technologies de recherche associées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f8a03738958e19712ff8cc4566e4b7f7396ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112471"
---
# <a name="related-search-technologies"></a>Technologies de recherche associées

Cette rubrique décrit les technologies liées à la [Recherche Windows](-search-3x-wds-overview.md).

Cette rubrique est organisée comme suit :

-   [Recherche d’entreprise](#enterprise-search)
    -   [Recherche SharePoint Enterprise](#sharepoint-enterprise-search)
-   [Windows Desktop Search 2. x](#windows-desktop-search-2x)
-   [Platform SDK : service d’indexation](#platform-sdk-indexing-service)
-   [Rubriques connexes](#related-topics)

## <a name="enterprise-search"></a>Recherche d’entreprise

Pour obtenir une vue d’ensemble des ressources techniques pour la [recherche d’entreprise auprès de Microsoft](https://www.microsoft.com/enterprisesearch/en/us/default.aspx), consultez :

-   [Centre de ressources de recherche d’entreprise](https://developer.microsoft.com/office/docs)
-   [Blog Microsoft Enterprise Search](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a>Recherche SharePoint Enterprise

SharePoint Foundation 2010 fournit des [requêtes à partir du code côté serveur](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) et des [requêtes à partir du code côté client](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14)). Pour plus d’informations sur l’interrogation, la recherche de nouveaux contenus et l’amélioration de la pertinence avec SharePoint Server 2010 Enterprise Search, consultez notions de base de la [recherche d’entreprise](/previous-versions/office/ee554857(v=office.14)).

La recherche Windows 7 prend en charge la Fédération de recherche aux magasins de données distants à l’aide des technologies OpenSearch, qui permettent aux utilisateurs d’accéder à leurs données distantes à partir de l’Explorateur Windows et d’interagir avec eux. SharePoint Search Server 2008 et MOSS 2007 SP2 prennent également en charge la recherche fédérée de serveurs distants à l’aide de OpenSearch. Pour plus d’informations sur le déploiement du serveur de recherche 2008 avec Office SharePoint Server 2007, consultez recherche [fédérée Search \[ Server \] 2008](/previous-versions/office/bb931109(v=office.14)). Pour plus d’informations sur la recherche par facettes MOSS, dans laquelle les résultats de la recherche sont retrouvés par catégorie, consultez [CodePlex](https://www.codeplex.com/FacetedSearch).

Les gestionnaires de protocoles de recherche Windows utilisent des spécifications de conception similaires à celles de SharePoint Server, et ils peuvent souvent être utilisés de manière interchangeable. Par conséquent, lorsque les utilisateurs doivent effectuer des recherches dans les bases de données héritées, les magasins de courrier électronique ou d’autres structures de données qui ne sont pas prises en charge par Windows Search, vous devez d’abord déterminer si un gestionnaire de protocole existe déjà pour ce magasin de données, peut-être pour une utilisation avec une autre application telle que SharePoint Server. Dans ce cas, vous pouvez installer ce gestionnaire de protocole sur le système.

## <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2. x

L’utilisation de et le développement des versions 2. x de Microsoft Windows Desktop Search (WDS) sont fortement déconseillées. Au lieu d’utiliser [Windows Desktop Search 2. x](../lwef/-search-2x-wds-overview.md), utilisez Windows [Search](-search-3x-wds-overview.md) et l' [API Windows Search](-search-reference-entry-page.md).

## <a name="platform-sdk-indexing-service"></a>Platform SDK : service d’indexation

[Platform SDK : le service d’indexation](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) est obsolète depuis Windows XP. Utilisez plutôt l’API [Windows Search et](-search-3x-wds-overview.md) [Windows Search](-search-reference-entry-page.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Guide du développeur Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Référence de recherche Windows](-search-reference-entry-page.md)
</dt> <dt>

[Exemples de code Windows Search](-search-samples-ovw.md)
</dt> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Glossaire Windows Search](search-glossary.md)
</dt> </dl>

 

 
