---
description: En savoir plus sur les paramètres de sauvegarde et de restauration
title: Paramètres de sauvegarde et de restauration
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6b82d3ffa1f55d79ac516ede469d422e7aced99
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982962"
---
# <a name="backup-and-restore-parameters"></a>Paramètres de sauvegarde et de restauration


_**S’applique à :** Windows | Windows Serveurs_

## <a name="backup-and-restore-parameters"></a>Paramètres de sauvegarde et de restauration

Cette rubrique contient les paramètres utilisés pour la sauvegarde et la restauration.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

Le chemin d’accès complet à chaque base de données est conservé dans les journaux des transactions au moment de l’exécution. En règle générale, ces bases de données doivent rester à l’emplacement d’origine pour que la relecture des transactions fonctionne correctement. Ce paramètre peut être utilisé pour forcer la récupération après incident ou une opération de restauration pour rechercher les bases de données référencées dans le journal des transactions dans le dossier spécifié.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>""</p> | 
| <p>Tapez :</p> | <p>Chemin d’accès au dossier (String)</p> | 
| <p>Plage valide :</p> | <p>0 – 246 caractères</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>No</p> | 
| <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramCleanupMismatchedLogFiles*  
77  

Ce paramètre contrôle le résultat de [JetInit](./jetinit-function.md) lorsque le moteur de base de données est configuré pour commencer à utiliser des fichiers du journal des transactions sur un disque d’une taille différente de celle configurée. Normalement, [JetInit](./jetinit-function.md) récupère correctement les bases de données, mais échoue avec JET_errLogFileSizeMismatchDatabasesConsistent pour indiquer que la taille du fichier journal est mal configurée. Toutefois, lorsque ce paramètre est défini sur true, le moteur de base de données supprime silencieusement tous les anciens fichiers journaux, démarre un nouvel ensemble de fichiers journaux de transactions à l’aide de la taille de fichier journal configurée et retourne JET_errSuccess.

Ce paramètre est utile lorsque l’application souhaite modifier en toute transparence la taille du fichier journal des transactions, tout en continuant à travailler de manière transparente dans les scénarios de mise à niveau et de restauration.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>Faux</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>Yes</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>No</p> | 
| <p>Disponibilité :</p> | <p>Tous</p> | 



*JET_paramDeleteOutOfRangeLogs*  
52  

Lorsque ce paramètre a la valeur true, tous les fichiers journaux des transactions trouvés sur le disque qui ne font pas partie de la séquence actuelle des fichiers journaux seront supprimés par [JetInit](./jetinit-function.md). Cela peut être utilisé pour nettoyer automatiquement les fichiers journaux superflus après une opération de restauration.

**Windows XP :**  introduite dans Windows XP.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>Faux</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>Yes</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>Yes</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramOSSnapshotTimeout*  
82  

Ce paramètre configure la durée autorisée entre un appel à [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) et [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) avant qu’un délai d’attente ne se produise. Pour plus d’informations, consultez [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) et [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) . Le délai d’attente est exprimé en millisecondes.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>20000 (Windows XP et Windows Server 2003);</p><p>70000 (Windows Server 2003 SP1)</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>0 – 2147483647</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Yes</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>No</p> | 
| <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramZeroDatabaseDuringBackup*  
71  

Lorsque ce paramètre a la valeur true, toutes les pages d’une base de données qui subit une sauvegarde en continu sont nettoyées des données supprimées. Il est important de noter que les pages de la base de données qui sont en cours de nettoyage sont sur le disque. Le jeu de données complet est sauvegardé avant le processus de nettoyage.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>Faux</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>Yes</p> | 
| <p>Affecte les ressources :</p> | <p>No</p> | 
| <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
