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
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530117"
---
# <a name="backup-and-restore-parameters"></a>Paramètres de sauvegarde et de restauration


_**S’applique à :** Windows | Serveur Windows_

## <a name="backup-and-restore-parameters"></a>Paramètres de sauvegarde et de restauration

Cette rubrique contient les paramètres utilisés pour la sauvegarde et la restauration.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

Le chemin d’accès complet à chaque base de données est conservé dans les journaux des transactions au moment de l’exécution. En règle générale, ces bases de données doivent rester à l’emplacement d’origine pour que la relecture des transactions fonctionne correctement. Ce paramètre peut être utilisé pour forcer la récupération après incident ou une opération de restauration pour rechercher les bases de données référencées dans le journal des transactions dans le dossier spécifié.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Chemin d’accès au dossier (String)</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0 – 246 caractères</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows XP et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramCleanupMismatchedLogFiles*  
77  

Ce paramètre contrôle le résultat de [JetInit](./jetinit-function.md) lorsque le moteur de base de données est configuré pour commencer à utiliser des fichiers du journal des transactions sur un disque d’une taille différente de celle configurée. Normalement, [JetInit](./jetinit-function.md) récupère correctement les bases de données, mais échoue avec JET_errLogFileSizeMismatchDatabasesConsistent pour indiquer que la taille du fichier journal est mal configurée. Toutefois, lorsque ce paramètre est défini sur true, le moteur de base de données supprime silencieusement tous les anciens fichiers journaux, démarre un nouvel ensemble de fichiers journaux de transactions à l’aide de la taille de fichier journal configurée et retourne JET_errSuccess.

Ce paramètre est utile lorsque l’application souhaite modifier en toute transparence la taille du fichier journal des transactions, tout en continuant à travailler de manière transparente dans les scénarios de mise à niveau et de restauration.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Faux</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Tous</p></td>
</tr>
</tbody>
</table>


*JET_paramDeleteOutOfRangeLogs*  
52  

Lorsque ce paramètre a la valeur true, tous les fichiers journaux des transactions trouvés sur le disque qui ne font pas partie de la séquence actuelle des fichiers journaux seront supprimés par [JetInit](./jetinit-function.md). Cela peut être utilisé pour nettoyer automatiquement les fichiers journaux superflus après une opération de restauration.

**Windows XP :**  Introduite dans Windows XP.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Faux</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows XP et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramOSSnapshotTimeout*  
82  

Ce paramètre configure la durée autorisée entre un appel à [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) et [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) avant qu’un délai d’attente ne se produise. Pour plus d’informations, consultez [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) et [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) . Le délai d’attente est exprimé en millisecondes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>20000 (Windows XP et Windows Server 2003);</p>
<p>70000 (Windows Server 2003 SP1)</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows XP et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramZeroDatabaseDuringBackup*  
71  

Lorsque ce paramètre a la valeur true, toutes les pages d’une base de données qui subit une sauvegarde en continu sont nettoyées des données supprimées. Il est important de noter que les pages de la base de données qui sont en cours de nettoyage sont sur le disque. Le jeu de données complet est sauvegardé avant le processus de nettoyage.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Faux</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows XP et versions ultérieures</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
