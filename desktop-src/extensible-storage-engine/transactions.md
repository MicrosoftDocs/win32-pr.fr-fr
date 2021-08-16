---
description: 'en savoir plus sur : Transactions (événements Windows)'
title: Transactions (événements Windows)
TOCTitle: Transactions
ms:assetid: 1ceb362c-1efe-439b-b10a-016c8a54f27b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269197(v=EXCHG.10)
ms:contentKeyID: 32765500
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e223c95d7f8af5a4350786891d58b72c508443e459990d413d5b46bc2e12a2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107054"
---
# <a name="transactions-windows-events"></a>Transactions (événements Windows)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="transactions"></a>Transactions

Les transactions ESE sont des unités logiques de traitement qui contrôlent la façon dont une application visualise et manipule des lignes dans la base de données. Votre application peut utiliser des points d’enregistrement de transaction pour déterminer s’il faut conserver ou ignorer un ensemble spécifique de modifications apportées à la base de données. Toutes les transactions dans ESE sont atomiques, cohérentes, isolées et durables (ACID) comme indiqué ci-dessous :

  - **Atomic :** Toutes les mises à jour de la transaction s’affichent dans la base de données ou elles sont ignorées.

<!-- end list -->

  - **Cohérent :** La base de données démarre toujours dans un état légal et se termine toujours par un autre état légal. Pour les applications ESE, le moteur de base de données contrôle certaines contraintes simples, par exemple l’unicité d’un index unique, mais l’application elle-même définit presque tous les autres aspects de ce que cela signifie que la base de données doit être dans un état légal.

<!-- end list -->

  - **Isolation :** Les transactions sont isolées des mises à jour par d’autres sessions. Une transaction ne verra jamais un ensemble partiel de modifications apportées par une autre transaction.

<!-- end list -->

  - **Durable :** Une fois que le moteur de base de données a confirmé qu’une transaction a été validée, ses modifications sont persistantes dans la base de données. La durabilité d’une transaction peut éventuellement être annulée pour des raisons de performances.

Les transactions sont effectuées dans les limites des appels à [JetBeginTransaction](./jetbegintransaction-function.md) et [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md). Lorsque l’application entre dans la transaction, la base de données apparaît figée à l’instance au moment où la transaction commence. C’est ce qu’on appelle l’isolation d’instantané. Si la transaction se termine par l’appel de [JetRollback](./jetrollback-function.md), aucune des opérations effectuées dans la transaction n’est validée dans la base de données. Si le processus ou l’ordinateur se bloque avant que [JetCommitTransaction](./jetcommittransaction-function.md) ne soit appelé, il revient à appeler [JetRollback](./jetrollback-function.md).

Cette procédure montre comment démarrer et valider une transaction qui lit et met à jour des données dans une base de données.

### <a name="to-start-and-commit-a-transaction"></a>Pour démarrer et valider une transaction

1.  Appelez [JetBeginTransaction](./jetbegintransaction-function.md) ou [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) avec l’ID de session pour démarrer la transaction.

2.  Déplacez le curseur vers l’enregistrement souhaité en appelant [JetMove](./jetmove-function.md) avec JET_MoveFirst spécifié dans le paramètre *cRow* . Pour plus d’informations sur le déplacement du curseur, consultez la rubrique [indexation dans le tableau](./indexing-in-the-table.md) .

3.  Appelez [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) sur l’enregistrement en cours avec JET_ColInfo spécifié dans le paramètre *InfoLevel* pour récupérer l’ID de colonne de la colonne. L’ID de colonne est retourné dans la structure [JET_COLUMNDEF](./jet-columndef-structure.md) .

4.  Appelez [JetSetColumn](./jetsetcolumn-function.md) avec l’ID de session, l’ID de table et l’ID de colonne de la colonne mise à jour. Les données de la colonne sont contenues dans le paramètre *pvData* .

5.  Appelez [JetCommitTransaction](./jetcommittransaction-function.md) pour valider la transaction dans la base de données.

La façon dont un moteur de base de données ESE implémente l’isolement de capture instantanée présente des différences importantes par rapport aux modèles d’isolation et de verrouillage de base de données relationnelle traditionnels. Lorsqu’une transaction lit une ligne, elle peut toujours accéder à la ligne sans échec ou en attendant que d’autres sessions libèrent un verrou. Lorsqu’une transaction tente de mettre à jour une ligne, elle est réussie s’il s’agit de la première session pour mettre à jour cette ligne, c’est-à-dire le premier enregistreur qui gagne. Si la session n’est pas le premier enregistreur, elle échoue immédiatement avec une erreur de conflit d’écriture. La session doit ensuite abandonner sa transaction, attendre (généralement via un délai aléatoire) pour que l’autre transaction valide ses modifications, puis retenter la transaction. Le moteur de base de données n’entraîne pas automatiquement l’attente de cette session jusqu’à la fin de la mise à jour de l’autre transaction. En règle générale, une transaction est testée si elle peut mettre à jour une ligne à l’intérieur de l’appel [JetUpdate](./jetupdate-function.md) . S’il ne peut pas verrouiller la ligne pour la mise à jour, [JetUpdate](./jetupdate-function.md) échouera avec JET_errWriteConflict.

Les sessions sont limitées à un thread à partir du moment où la transaction commence jusqu’à la fin de la transaction. Il est recommandé que toutes les opérations de mise à jour et de récupération soient effectuées dans une transaction. ESE prend également en charge les modifications de schéma, telles que la création de tables et l’ajout de colonnes à l’intérieur de la transaction. Les modifications de mise à jour et de schéma peuvent être effectuées dans la même transaction. Une fois la transaction terminée avec [JetCommitTransaction](./jetcommittransaction-function.md), la mise à jour est consignée dans le fichier journal des transactions. Ces fichiers peuvent être utilisés pour maintenir un État logiquement cohérent en cas d’arrêt inattendu d’un processus ou d’un arrêt du système.

Les transactions peuvent être imbriquées jusqu’à 7 niveaux avec des appels correspondants à [JetBeginTransaction](./jetbegintransaction-function.md) et [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) imbriqués les uns dans les autres. Cela permet à l’application de restaurer une partie de la transaction sans devoir revenir à la totalité de la transaction. L’appel imbriqué à [JetCommitTransaction](./jetcommittransaction-function.md) signifie que ce niveau de traitement est terminé ; Toutefois, la transaction n’est pas validée dans la base de données jusqu’à l’appel externe le plus élevé pour valider la transaction avec [JetCommitTransaction](./jetcommittransaction-function.md).

Les colonnes de mise à jour du tiers de confiance peuvent être mises à jour simultanément par plusieurs sessions sans échec avec Jet_errWriteConflict. La fonction [JetEscrowUpdate](./jetescrowupdate-function.md) peut uniquement être appelée sur des colonnes de dépôt, colonnes créées avec Jet_bitColumnEscrowUpdate.
