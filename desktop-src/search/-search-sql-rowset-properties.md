---
description: Une fois qu’un résultat est retourné à partir d’une requête, vous pouvez accéder à plusieurs propriétés de l’ensemble de lignes.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Propriétés du rowset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515212"
---
# <a name="rowset-properties"></a>Propriétés du rowset

Une fois qu’un résultat est retourné à partir d’une requête, vous pouvez accéder à plusieurs propriétés de l’ensemble de lignes.

En plus des propriétés de l’ensemble de lignes OLE-DB standard, Windows Search SQL offre les quatre propriétés personnalisées suivantes. Le GUID de ce jeu de propriétés est {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.

Windows Search prend en charge la propriété OLE-DB standard DBPROP \_ COMMANDTIMEOUT du jeu de propriétés d' [ensemble de \_ lignes DBPROPSET](/previous-versions//ms691738(v=vs.85)) .



| Nom de la propriété                  | PROPID/type | Description                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DONOTCOMPUTEEXPENSIVEPROPS     | booléen 15/VT \_ | L’affectation de la valeur true empêche le calcul des propriétés coûteuses telles que les résultats trouvés et le classement maximal qui nécessitent l’évaluation de l’ensemble de la requête lorsqu’une propriété d’ensemble de lignes est accédée.                                                                                                                                                                         |
| Rang maximal (rang MAX. \_ )       | 6/VT \_ I4    | Classement le plus élevé calculé pour tous les résultats.                                                                                                                                                                                                                                                                                                          |
| Résultats trouvés (résultats \_ trouvés) | 7/VT \_ I4    | Nombre total d’éléments uniques pour cette requête. Pour une requête SELECT, il s’agit du nombre d’éléments dans l’ensemble de lignes. Pour un groupe sur une requête, il s’agit du nombre d’éléments feuille uniques. Cette propriété n’identifie pas le nombre de lignes dans l’ensemble de lignes de niveau supérieur (le nombre de groupes de niveau supérieur).                                                        |
| Où ID (WHEREID)             | 8/VT \_ I4    | Identificateur des restrictions utilisées pour une requête. Si un ensemble de lignes est ouvert lors de l’exécution d’une nouvelle requête, la nouvelle requête peut réutiliser les restrictions de l’ancienne requête, tirant ainsi parti du travail déjà effectué. Pour plus d’informations sur la réutilisation des restrictions WHERE, référez-vous à la [fonction ReuseWhere](-search-sql-reusewhere.md). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Indexation des événements d’ensemble de priorités et d’ensembles de lignes dans Windows 7](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
