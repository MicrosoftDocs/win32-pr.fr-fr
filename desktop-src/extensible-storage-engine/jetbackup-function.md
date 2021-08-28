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
ms.openlocfilehash: e17ee5029da8ac71b5421e44a3647494e676ba71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982992"
---
# <a name="jetbackup-function"></a>Fonction JetBackup


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetbackup-function"></a>Fonction JetBackup

La fonction **JetBackup** crée une sauvegarde de la base de données pendant que la base de données est en ligne. cette fonction est principalement utilisée à des fins de compatibilité descendante avec Windows 2000 et des moteurs de base de données antérieurs, où une seule instance de base de données est autorisée. Dans ce cas, l’instance active est l’instance qui est sauvegardée.

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


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Crée une sauvegarde complète de la base de données. Cela permet la conservation d’une sauvegarde existante dans le même répertoire en cas d’échec de la nouvelle sauvegarde.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Crée une sauvegarde incrémentielle par opposition à une sauvegarde complète. Cela signifie que seuls les fichiers journaux depuis la dernière sauvegarde complète ou incrémentielle sont sauvegardés.</p> | 



*pfnStatus*

Pointeur vers la fonction de rappel [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , qui fournit des informations de notification sur la progression de l’opération de sauvegarde.

### <a name="return-value"></a>Valeur renvoyée

La fonction retourne l’un des codes d’erreur [JET_ERR](./jet-err.md) . Les éléments suivants sont les plus couramment renvoyés. (pour obtenir la liste complète des erreurs pour cette API, consultez [Codes d’erreur du moteur d’Stockage Extensible](./extensible-storage-engine-error-codes.md).)


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Une sauvegarde est déjà en cours pour la même instance. Plusieurs sauvegardes ne sont pas autorisées en même temps.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>L’instance n’est pas encore prête pour la sauvegarde lors de son initialisation.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong> cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errInvalidBackup</p> | <p>Une sauvegarde incrémentielle n’est pas autorisée si l’enregistrement circulaire est activé.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Les options spécifiées ne sont pas valides.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un paramètre non valide a été passé dans l’API.</p> | 
| <p>JET_errInvalidPath</p> | <p>Le chemin d’accès de destination n’existe pas.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>L’instance est en cours d’exécution sans journalisation. Aucune sauvegarde n’est autorisée.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>Une erreur de vérification de la somme de contrôle s’est produite sur un fichier journal.</p> | 
| <p>JET_errLogWriteFail</p> | <p>La journalisation de l’instance est désactivée de façon temporaire ou définitive en raison d’une erreur inattendue.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errReadVerifyFailure</p> | <p>Une erreur de vérification de la somme de contrôle s’est produite sur une page de base de données.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p><strong>Windows XP :</strong> cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance associée à la session est en cours d’arrêt.</p> | 



Si la fonction s’exécute correctement, tous les fichiers nécessaires à une restauration jusqu’au moment de la sauvegarde seront contenus dans le répertoire de sauvegarde. S’il s’agit d’une sauvegarde complète, les fichiers sont les fichiers de base de données et les fichiers journaux nécessaires pour ramener la base de données à un état cohérent. S’il s’agit d’une sauvegarde incrémentielle, seuls les fichiers journaux sont ajoutés aux répertoires, mais les fichiers déjà existants (bases de données et fichiers journaux), ainsi que les nouveaux fichiers journaux, peuvent être restaurés pour ramener la base de données dans l’État où elle se trouvait au moment où la sauvegarde a commencé.

En tant qu’effet secondaire de la sauvegarde, les fichiers journaux qui ne sont plus nécessaires sont tronqués.

En même temps, les en-têtes de base de données sont mis à jour avec les informations lors de la dernière sauvegarde.

Si la fonction échoue, il n’y aura aucun fichier dans la destination du répertoire de sauvegarde, aucune restauration n’est donc possible. En même temps, les fichiers journaux actuels ne seront pas tronqués.

#### <a name="remarks"></a>Remarques

Les différentes étapes de la sauvegarde auront des entrées de journal des événements générées, y compris les noms de fichiers, la troncation du journal et le résultat final de la sauvegarde.

Les sauvegardes incrémentielles sont possibles uniquement après la prise d’une sauvegarde complète. En outre, les sauvegardes incrémentielles sont possibles uniquement si la journalisation circulaire est désactivée. Il est recommandé que le répertoire de sauvegarde ne contienne aucun fichier autre que celui utilisé dans la sauvegarde ou ajouté par une sauvegarde précédente réussie.

Le répertoire de sauvegarde doit exister, sauf si le paramètre *JET_paramCreatePathIfNotExist* est défini pour l’instance. Pour plus d’informations, consultez [paramètres système](./extensible-storage-engine-system-parameters.md).

la sauvegarde effectue une vérification de la somme de contrôle sur toutes les pages de base de données utilisées et à partir de Windows Server 2003, également sur les fichiers journaux. Cela donne la possibilité d’estimer l’intégrité de la base de données, même pour les pages qui ne sont pas lues pendant des opérations normales. Si une telle altération est détectée, la sauvegarde échoue.

Pendant la sauvegarde, le fichier journal actuel est terminé et un nouveau journal est généré. De cette façon, tous les fichiers journaux nécessaires peuvent être des copies, car le journal actuel n’est plus utilisé.

Il est vivement recommandé de ne pas utiliser la sauvegarde à des fins autres que la sauvegarde et la restauration au niveau du moteur. Cela réduira le risque d’obtenir des erreurs pendant les opérations de sauvegarde et de restauration.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetBackupW</strong> (Unicode) et <strong>JetBackupA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
