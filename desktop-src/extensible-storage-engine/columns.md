---
description: 'En savoir plus sur : colonnes'
title: Colonnes
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 86f7d2bbb3925434ddbfff52e987b6e408af9ed8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531424"
---
# <a name="columns"></a>Colonnes


_**S’applique à :** Windows | Windows Serveurs_

## <a name="columns"></a>Colonnes

Une table peut être créée avec un ensemble initial de colonnes en appelant [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou sans un ensemble initial de colonnes en appelant [JetCreateTable](./jetcreatetable-function.md). Dans ESE, les tables peuvent contenir jusqu’à 127 colonnes de longueur fixe, 128 colonnes de longueur variable et 64 993 colonnes avec balises. Les colonnes sont identifiées par leur nom et leur ID et peuvent être ajoutées de manière dynamique à la table à l’aide de [JetAddColumn](./jetaddcolumn-function.md). Les colonnes sont créées avec un type de données spécifique et un ensemble facultatif d’attributs, par exemple si la colonne est de longueur fixe ou si elle peut être NULL ou non.

Le type d’une colonne détermine les données qui peuvent être stockées dans la colonne et de nombreuses propriétés de la colonne, y compris son ordre d’indexation. ESE prend en charge un large éventail de types de colonnes, dont la taille est comprise entre 1 et 2 Go (2146483647 caractères ASCII ou 1073741823 caractères Unicode). Pour obtenir la liste complète des types de données de colonne pris en charge par ESE, consultez la rubrique [JET_COLTYP](./jet-coltyp.md) . Les rubriques ci-dessous décrivent quelques-uns des types de colonnes pris en charge par ESE :

  - [Colonnes avec balises, fixes et variables](./tagged-fixed-and-variable-columns.md)

  - [Colonnes version, incrémentation automatique et tiers de confiance](./version-auto-increment-and-escrow-columns.md)

  - [Colonnes de valeur longue](./long-value-columns.md)

  - [Colonnes éparses à valeurs multiples](./multi-valued-sparse-columns.md)

  - [Colonnes définies par l’utilisateur](./user-defined-columns.md)

  - [Utilisation de colonnes dans une table](./using-columns-in-a-table.md)
