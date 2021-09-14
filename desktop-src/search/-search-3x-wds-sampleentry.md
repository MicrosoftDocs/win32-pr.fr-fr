---
description: cette rubrique décrit les technologies liées à la recherche de Windows.
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: Technologies de recherche associées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f8a03738958e19712ff8cc4566e4b7f7396ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231263"
---
# <a name="related-search-technologies"></a>Technologies de recherche associées

cette rubrique décrit les technologies liées à la [recherche de Windows](-search-3x-wds-overview.md).

Cette rubrique est organisée comme suit :

-   [Enterprise Recherche](#enterprise-search)
    -   [recherche de Enterprise SharePoint](#sharepoint-enterprise-search)
-   [Windows Desktop Search 2. x](#windows-desktop-search-2x)
-   [Platform SDK : service d’indexation](#platform-sdk-indexing-service)
-   [Rubriques connexes](#related-topics)

## <a name="enterprise-search"></a>Enterprise Recherche

pour obtenir une vue d’ensemble des ressources techniques pour la [recherche de Enterprise à partir de Microsoft](https://www.microsoft.com/enterprisesearch/en/us/default.aspx), consultez :

-   [Enterprise Rechercher dans le centre de ressources](https://developer.microsoft.com/office/docs)
-   [Blog Microsoft Enterprise Search](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a>recherche de Enterprise SharePoint

SharePoint Foundation 2010 fournit des [requêtes à partir du code côté serveur](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) et des [requêtes à partir du code côté client](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14)). pour plus d’informations sur l’interrogation, la recherche de nouveaux contenus et l’amélioration de la pertinence avec Sharepoint Server 2010 Enterprise search, consultez principes de base de la [recherche Enterprise](/previous-versions/office/ee554857(v=office.14)).

Windows 7 search prend en charge la fédération des recherches dans des magasins de données distants à l’aide de technologies OpenSearch, qui permettent aux utilisateurs d’accéder à leurs données distantes à partir d’Windows Explorer et d’interagir avec eux. SharePoint Search Server 2008 et MOSS 2007 SP2 prennent également en charge la recherche fédérée de serveurs distants à l’aide de OpenSearch. pour plus d’informations sur le déploiement du serveur de recherche 2008 avec Office SharePoint server 2007, voir serveur de recherche de recherche [fédérée \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)). Pour plus d’informations sur la recherche par facettes MOSS, dans laquelle les résultats de la recherche sont retrouvés par catégorie, consultez [CodePlex](https://www.codeplex.com/FacetedSearch).

Windows les gestionnaires de protocoles de recherche utilisent des spécifications de conception similaires à SharePoint Server et peuvent souvent être utilisés de manière interchangeable. par conséquent, lorsque les utilisateurs doivent effectuer des recherches dans les bases de données héritées, les magasins de courrier électronique ou d’autres structures de données qui ne sont pas prises en charge par Windows recherche, vous devez d’abord déterminer si un gestionnaire de protocole existe déjà pour ce magasin de données, peut-être pour une utilisation avec une autre application telle que SharePoint Server. Dans ce cas, vous pouvez installer ce gestionnaire de protocole sur le système.

## <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2. x

l’utilisation de et le développement des versions 2. x de Microsoft Windows Desktop Search (WDS) sont fortement déconseillées. au lieu d’utiliser [Windows Desktop search 2. x](../lwef/-search-2x-wds-overview.md), utilisez [Windows recherche](-search-3x-wds-overview.md) et l' [API de recherche Windows](-search-reference-entry-page.md).

## <a name="platform-sdk-indexing-service"></a>Platform SDK : service d’indexation

[platform SDK : le Service d’indexation](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) est obsolète à partir de Windows XP. au lieu de cela, utilisez [Windows recherche](-search-3x-wds-overview.md) et l' [API de recherche Windows](-search-reference-entry-page.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Rechercher dans le Guide du développeur](-search-developers-guide-entry-page.md)
</dt> <dt>

[Windows Référence de recherche](-search-reference-entry-page.md)
</dt> <dt>

[Windows Rechercher des exemples de code](-search-samples-ovw.md)
</dt> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Windows Rechercher dans le Glossaire](search-glossary.md)
</dt> </dl>

 

 
