---
description: 'En savoir plus sur : fonction JetBackup'
title: Fonction JetBackup
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531192"
---
# <a name="jetbackup-function"></a>Fonction JetBackup


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetbackup-function"></a>Fonction JetBackup

La fonction **JetBackup** crée une sauvegarde de la base de données pendant que la base de données est en ligne. Cette fonction est principalement utilisée à des fins de compatibilité descendante avec Windows 2000 et des moteurs de base de données antérieurs, où une seule instance de base de données est autorisée. Dans ce cas, l’instance active est l’instance qui est sauvegardée.

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Paramètres

*szBackupPath*

Répertoire dans lequel la sauvegarde est stockée. Si le chemin d’accès de sauvegarde est NULL, la fonction tronque les journaux, si possible.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Crée une sauvegarde complète de la base de données. Cela permet la conservation d’une sauvegarde existante dans le même répertoire en cas d’échec de la nouvelle sauvegarde.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Crée une sauvegarde incrémentielle par opposition à une sauvegarde complète. Cela signifie que seuls les fichiers journaux depuis la dernière sauvegarde complète ou incrémentielle sont sauvegardés.</p></td>
</tr>
</tbody>
</table>


*pfnStatus*

Pointeur vers la fonction de rappel [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , qui fournit des informations de notification sur la progression de l’opération de sauvegarde.

### <a name="return-value"></a>Valeur renvoyée

La fonction retourne l’un des codes d’erreur [JET_ERR](./jet-err.md) . Les éléments suivants sont les plus couramment renvoyés. (Pour obtenir la liste complète des erreurs pour cette API, consultez [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md).)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Code de retour</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>L’opération s’est terminée avec succès.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress</p></td>
<td><p>Une sauvegarde est déjà en cours pour la même instance. Plusieurs sauvegardes ne sont pas autorisées en même temps.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>L’instance n’est pas encore prête pour la sauvegarde lors de son initialisation.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>Une sauvegarde incrémentielle n’est pas autorisée si l’enregistrement circulaire est activé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Les options spécifiées ne sont pas valides.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un paramètre non valide a été passé dans l’API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Le chemin d’accès de destination n’existe pas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>L’instance est en cours d’exécution sans journalisation. Aucune sauvegarde n’est autorisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Une erreur de vérification de la somme de contrôle s’est produite sur un fichier journal.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogWriteFail</p></td>
<td><p>La journalisation de l’instance est désactivée de façon temporaire ou définitive en raison d’une erreur inattendue.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Une erreur de vérification de la somme de contrôle s’est produite sur une page de base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p>
<p><strong>Windows XP :  </strong> Cette valeur de retour est introduite dans Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>L’opération ne peut pas se terminer car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


Si la fonction s’exécute correctement, tous les fichiers nécessaires à une restauration jusqu’au moment de la sauvegarde seront contenus dans le répertoire de sauvegarde. S’il s’agit d’une sauvegarde complète, les fichiers sont les fichiers de base de données et les fichiers journaux nécessaires pour ramener la base de données à un état cohérent. S’il s’agit d’une sauvegarde incrémentielle, seuls les fichiers journaux sont ajoutés aux répertoires, mais les fichiers déjà existants (bases de données et fichiers journaux), ainsi que les nouveaux fichiers journaux, peuvent être restaurés pour ramener la base de données dans l’État où elle se trouvait au moment où la sauvegarde a commencé.

En tant qu’effet secondaire de la sauvegarde, les fichiers journaux qui ne sont plus nécessaires sont tronqués.

En même temps, les en-têtes de base de données sont mis à jour avec les informations lors de la dernière sauvegarde.

Si la fonction échoue, il n’y aura aucun fichier dans la destination du répertoire de sauvegarde, aucune restauration n’est donc possible. En même temps, les fichiers journaux actuels ne seront pas tronqués.

#### <a name="remarks"></a>Notes

Les différentes étapes de la sauvegarde auront des entrées de journal des événements générées, y compris les noms de fichiers, la troncation du journal et le résultat final de la sauvegarde.

Les sauvegardes incrémentielles sont possibles uniquement après la prise d’une sauvegarde complète. En outre, les sauvegardes incrémentielles sont possibles uniquement si la journalisation circulaire est désactivée. Il est recommandé que le répertoire de sauvegarde ne contienne aucun fichier autre que celui utilisé dans la sauvegarde ou ajouté par une sauvegarde précédente réussie.

Le répertoire de sauvegarde doit exister, sauf si le paramètre *JET_paramCreatePathIfNotExist* est défini pour l’instance. Pour plus d’informations, consultez [paramètres système](./extensible-storage-engine-system-parameters.md).

La sauvegarde effectue une vérification de la somme de contrôle sur toutes les pages de base de données utilisées et à partir de Windows Server 2003, également sur les fichiers journaux. Cela donne la possibilité d’estimer l’intégrité de la base de données, même pour les pages qui ne sont pas lues pendant des opérations normales. Si une telle altération est détectée, la sauvegarde échoue.

Pendant la sauvegarde, le fichier journal actuel est terminé et un nouveau journal est généré. De cette façon, tous les fichiers journaux nécessaires peuvent être des copies, car le journal actuel n’est plus utilisé.

Il est vivement recommandé de ne pas utiliser la sauvegarde à des fins autres que la sauvegarde et la restauration au niveau du moteur. Cela réduira le risque d’obtenir des erreurs pendant les opérations de sauvegarde et de restauration.

#### <a name="requirements"></a>Configuration requise

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
<tr class="even">
<td><p><strong>Bibliothèque</strong></p></td>
<td><p>Utilisez ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetBackupW</strong> (Unicode) et <strong>JetBackupA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[Fichiers ESE (Extensible Storage Engine)](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
