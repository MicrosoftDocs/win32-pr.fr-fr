---
description: 'En savoir plus sur les éléments suivants : descripteurs ESE'
title: Handles ESE
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cc91a4586fc1619c55b5f45afbca39ce04c0c6cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010309"
---
# <a name="ese-handles"></a>Handles ESE


_**S’applique à :** Windows | Windows Serveurs_

## <a name="ese-handles"></a>Handles ESE

Les descripteurs ESE sont utilisés pour créer des sessions et accéder aux bases de données. Elles sont conservées dans une hiérarchie, ce qui signifie que la sortie d’un niveau est utilisée pour accéder aux ressources au niveau suivant.

Le diagramme ci-dessous montre la hiérarchie des handles et les fonctions correspondantes qui créent les handles. Également indiqué avec les fonctions, les handles utilisés dans l’appel permettent de créer le nouveau handle.

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

Comme indiqué dans le diagramme, l’instance est le handle racine et le niveau auquel la base de données est récupérée en cas d’arrêt inattendu d’un processus ou d’un arrêt du système. Le descripteur d’instance, JET_INSTANCE, est créé par [JetCreateInstance](./jetcreateinstance-function.md) et [JetCreateInstance2](./jetcreateinstance2-function.md). Le niveau suivant, le niveau de session, est le contexte de transaction du moteur de base de données et le niveau sous lequel toutes les opérations de base de données sont effectuées. Le descripteur de session, JET_SESID, est créé dans le contexte de l’instance dans l’appel à [JetBeginSession](./jetbeginsession-function.md). L’ID de session est utilisé dans tous les appels suivants pour accéder aux tables et aux bases de données. Si l’instance est utilisée par plusieurs threads à la fois, chaque thread doit utiliser son propre handle de session. Le descripteur de base de données est créé à l’aide du descripteur de session et principalement utilisé pour gérer le schéma de la base de données, mais il peut également être utilisé pour gérer des tables dans la base de données. Les descripteurs de base de données ne peuvent être utilisés que dans la session dans laquelle ils sont créés. Le descripteur de la base de données est créé dans l’appel à [JetCreateDatabase](./jetcreatedatabase-function.md) ou [JetOpenDatabase](./jetopendatabase-function.md). Les tables sont associées à l’ID de base de données sous lequel elles sont créées.

Le type de données JET_TABLEID contient un handle vers un curseur de base de données. Il permet d’analyser des enregistrements, de rechercher des enregistrements ou de créer des enregistrements de mise à jour et de suppression. Le descripteur de table est créé dans l’appel à [JetOpenTable](./jetopentable-function.md)ou [JetCreateTable](./jetcreatetable-function.md). [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)et [JetOpenTempTable3](./jetopentemptable3-function.md) créent également des ID de table pour les tables temporaires, et [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) et [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) retournent des ID de table dans la structure out. Les colonnes créées dans la table ont chacune un identificateur de colonne unique ou COLUMN_ID. Les ID des colonnes sont créés dans les appels à [JetAddColumn](./jetaddcolumn-function.md), ou dans les appels à [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)ou [JetOpenTempTable3](./jetopentemptable3-function.md) pour les tables temporaires. Les ID de colonne peuvent également être récupérés pour une colonne donnée par nom avec des API telles que [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).
