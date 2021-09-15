---
description: Microsoft Windows Search, basé sur les normes SQL-92 et SQL-99, améliore les recherches en texte intégral dans les applications de gestion de documents ou de gestion des connaissances.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: SQL Extensions dans Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523396"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a>SQL Extensions dans Microsoft Windows Search

Microsoft Windows Search, basé sur les normes SQL-92 et SQL-99, améliore les recherches en texte intégral dans les applications de gestion de documents ou de gestion des connaissances. Windows Les améliorations de la recherche sont les suivantes :

## <a name="128-character-identifier-names"></a>128-noms d’identificateurs de caractères

bien que les SQL-92 et SQL-99 restreignent la colonne et d’autres identificateurs à 18 caractères, Windows recherche prend en charge les noms de colonnes de 128 caractères. Pour plus d’informations, consultez [Identificateurs](-search-sql-identifiers.md).

## <a name="grouping-results-by-columns"></a>Regroupement des résultats par colonnes

Les requêtes peuvent spécifier la façon dont les résultats doivent être regroupés. Vous pouvez spécifier les plages selon lesquelles effectuer un regroupement, et vous pouvez spécifier plusieurs colonnes pour le regroupement. Par exemple, vous pouvez regrouper les résultats sur une plage de tailles de fichier (taille < 100, 100 <= taille < 1000 ; 1000 <= taille) et vous pouvez imbriquer des regroupements. Pour plus d’informations, consultez [regrouper sur... ... Instruction](-search-sql-group-on-over.md).

## <a name="diacritic-insensitive-searching"></a>Recherche Diacritic-Insensitive

en plus de la recherche qui ne respecte pas la casse, Windows recherche prend en charge la recherche qui ne respecte pas les signes diacritiques (accents). Pour plus d’informations, consultez [sensibilité des signes diacritiques dans les recherches](-search-sql-accentinsensitivitysearches.md).

## <a name="column-weighting"></a>Pondération de colonne

Les requêtes qui recherchent plusieurs colonnes peuvent spécifier l’importance de chaque colonne. Les prédicats [Contains](-search-sql-contains.md) et [FREETEXT](-search-sql-freetext.md) prennent en charge la pondération de colonne.

## <a name="null-predicate"></a>Prédicat NULL

Bien que l’indexation du contenu de texte intégral n’ait aucun ensemble de colonnes défini, les requêtes peuvent exiger que les membres du jeu de résultats n’aient pas de colonnes spécifiées. Il n’est pas possible de faire la différence entre un document a une propriété spécifiée avec la valeur définie sur **null** et un document qui n’a pas de propriété.

## <a name="rank-modification"></a>Modification de classement

Vous pouvez manipuler le classement des résultats de recherche à l’aide de [pondérations](-search-sql-understandingrelevancevalues.md) sur les propriétés et sur des groupes de propriétés avec alias. La contrainte de classement prend en charge la manipulation directe du classement de pertinence en fonction des critères que vous spécifiez.

 

 



