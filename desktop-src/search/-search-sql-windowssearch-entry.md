---
description: Windows Search fournit des fonctionnalités d’analyse de contenu et de recherche qui prennent en charge la recherche en texte intégral. Le langage de requête utilisé par Windows Search étend la syntaxe de requête de base de données SQL-92 et SQL-99 standard pour améliorer son utilité avec les recherches textuelles.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Interrogation de l’index avec la syntaxe SQL de Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484409"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a>Interrogation de l’index avec la syntaxe SQL de Windows Search

Windows Search fournit des fonctionnalités d’analyse de contenu et de recherche qui prennent en charge la recherche en texte intégral. Le langage de requête utilisé par Windows Search étend la syntaxe de requête de base de données SQL-92 et SQL-99 standard pour améliorer son utilité avec les recherches textuelles.

Toutes les fonctionnalités de la langage SQL de recherche Windows (SQL) sont compatibles avec Windows Search sur Windows Vista et versions ultérieures, y compris toutes les versions de Windows 10.

Cette section fournit une vue d’ensemble de la syntaxe SQL dans Windows Search et inclut les rubriques suivantes :

- [Vue d’ensemble de la syntaxe SQL de Windows Search](-search-sql-ovwofsearchquery.md)
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

L’exemple de code WSSQL montre comment communiquer entre Microsoft OLE DB et Windows Search via SQL. L’exemple de code WSOleDB illustre Active Template Library (ATL) OLE DB l’accès aux applications Windows Search et deux méthodes supplémentaires pour récupérer les résultats de Windows Search. Les deux exemples sont disponibles dans les [exemples Windows Search](-search-samples-ovw.md) et le [Kit de développement logiciel (SDK) Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

## <a name="related-topics"></a>Rubriques connexes

[Interrogation de l’index programmatiquement](-search-3x-wds-qryidx-overview.md)

[Utilisation des approches SQL et AQS pour interroger l’index](-search-3x-wds-qryidx-overview.md)

[Interrogation de l’index avec ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

[Interrogation de l’index avec le protocole search-ms](-search-3x-wds-qryidx-searchms.md)

[Interrogation de l’index avec la syntaxe SQL de Windows Search](-search-sql-windowssearch-entry.md)

[Utilisation de la syntaxe de requête avancée par programmation](-search-3x-advancedquerysyntax.md)
