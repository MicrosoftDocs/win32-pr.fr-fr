---
description: 'En savoir plus sur : l’indexation dans la table'
title: Indexation dans la table
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 8bfc5054e5fd2b2f13747b0b5729987b9f81d5c21aa2faf38385b11e757f6763
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721449"
---
# <a name="indexing-in-the-table"></a>Indexation dans la table


_**S’applique à :** Windows | Windows Serveurs_

## <a name="indexing-in-the-table"></a>Indexation dans la table

Un index est un ensemble de colonnes clés qui définissent un classement permanent des enregistrements dans une table. Les enregistrements sont des entrées d’index dans l’index primaire. Un index principal et plusieurs index secondaires peuvent être définis pour créer des ordres de données différents dans la table.

Bien qu’il soit possible de définir plusieurs index, les enregistrements sont physiquement stockés dans les arborescences B + dans l’ordre spécifié par l’index primaire. L’index primaire est toujours un index cluster et doit également être unique. L’index primaire doit être déclaré avant la première mise à jour de la table afin de conserver le classement de l’index. Quand aucun index primaire n’est défini par l’application, les données sont stockées dans l’ordre dans lequel les enregistrements sont ajoutés à la table. Cet index spécial est désigné sous le terme d’index séquentiel.

Les arborescences B + séparées sont utilisées pour trier les enregistrements en fonction de l’index secondaire. Les entrées d’index de l’index secondaire contiennent des pointeurs vers les données stockées en fonction de l’index primaire. Les entrées d’index des enregistrements de l’index primaire doivent être uniques, car l’index secondaire pointe vers l’enregistrement à l’aide de la clé primaire de l’enregistrement. Les index secondaires peuvent avoir ou non une contrainte d’unicité. Pour plus d’informations, consultez la rubrique [vue d’ensemble de la base de données](./database-overview.md) .
