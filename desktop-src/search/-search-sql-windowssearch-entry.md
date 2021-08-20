---
description: Windows La recherche fournit des fonctionnalités d’analyse de contenu et de recherche qui prennent en charge la recherche en texte intégral. le langage de requête utilisé par Windows Search étend la syntaxe de requête de base de données standard SQL-92 et SQL-99 pour améliorer son utilité avec les recherches textuelles.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: interrogation de l’Index avec Windows syntaxe de SQL de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2687e5b35e12dd70cca332de92aa19c466907f102f69373e320c6e8162a3dcf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051612"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a>interrogation de l’Index avec Windows syntaxe de SQL de recherche

Windows La recherche fournit des fonctionnalités d’analyse de contenu et de recherche qui prennent en charge la recherche en texte intégral. le langage de requête utilisé par Windows Search étend la syntaxe de requête de base de données standard SQL-92 et SQL-99 pour améliorer son utilité avec les recherches textuelles.

toutes les fonctionnalités de Windows langage SQL de recherche (SQL) sont compatibles avec la recherche de Windows sur Windows Vista et versions ultérieures, y compris toutes les versions de Windows 10.

cette section fournit une vue d’ensemble de la syntaxe de SQL dans Windows Search et inclut les rubriques suivantes :

- [vue d’ensemble de la syntaxe de SQL de recherche Windows](-search-sql-ovwofsearchquery.md)
- [Informations générales sur le langage de requête](-search-sql-generalqueryinfo.md)
- [REGROUPER... ... Gestion](-search-sql-group-on-over.md)
- [Instruction SELECT](-search-sql-select.md)
- [FROM, clause](-search-sql-from.md)
- [Clause WHERE](-search-sql-where.md)
- [Clause ORDER BY](-search-sql-orderby.md)
- [RANK BY, clause](-search-sql-rankby.md)
- [Instruction SET](-search-sql-set.md)
- [Propriétés du rowset](-search-sql-rowset-properties.md)

Cette documentation suppose que vous êtes familiarisé avec la fonction de liaison et d’incorporation d’objets (OLE DB) et SQL.

## <a name="code-samples"></a>Exemples de code

l’exemple de code WSSQL montre comment communiquer entre Microsoft OLE DB et Windows Search via SQL. l’exemple de code WSOleDB illustre Active Template Library (ATL) OLE DB l’accès aux applications de recherche Windows, ainsi que deux méthodes supplémentaires pour récupérer les résultats de Windows recherche. les deux exemples sont disponibles dans les [exemples de recherche Windows](-search-samples-ovw.md) et le [kit de développement logiciel (SDK) Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

## <a name="related-topics"></a>Rubriques connexes

[Interrogation de l’index programmatiquement](-search-3x-wds-qryidx-overview.md)

[utilisation d’approches SQL et AQS pour interroger l’Index](-search-3x-wds-qryidx-overview.md)

[Interrogation de l’index avec ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

[Interrogation de l’index avec le protocole search-ms](-search-3x-wds-qryidx-searchms.md)

[interrogation de l’Index avec Windows syntaxe de SQL de recherche](-search-sql-windowssearch-entry.md)

[Utilisation de la syntaxe de requête avancée par programmation](-search-3x-advancedquerysyntax.md)
