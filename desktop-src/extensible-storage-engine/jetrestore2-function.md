---
description: 'En savoir plus sur : fonction JetRestore2'
title: Fonction JetRestore2
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5bcc515dc3c5d93874913dfd8997b1f5dffa76db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471345"
---
# <a name="jetrestore2-function"></a>Fonction JetRestore2


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetrestore2-function"></a>Fonction JetRestore2

**JetRestore2** restaure et récupère une sauvegarde en continu d’une instance, y compris toutes les bases de données attachées. cette fonction est principalement utilisée à des fins de compatibilité descendante avec Windows 2000 et des moteurs de base de données antérieurs, où une seule instance de base de données est autorisée. Dans ce cas, l’instance active est l’instance qui est restaurée.

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Paramètres

*SZ*

Dossier dans lequel se trouve la sauvegarde. La sauvegarde doit avoir été générée à l’aide des API [JetBackup](./jetbackup-function.md) .

*szDest*

Nom du dossier dans lequel les fichiers de base de données du jeu de sauvegarde seront copiés et récupérés. Si la valeur est NULL (ce qui est le cas pour le [JetRestore](./jetrestore-function.md)hérité), les fichiers de base de données sont copiés et récupérés à leur emplacement d’origine.

*PFN*

Pointeur facultatif vers la fonction qui sera appelée en tant qu’informations de notification sur la progression de l’opération de restauration.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>L’opération a échoué, car le moteur est déjà initialisé pour cette instance.</p> | 
| <p>JET_errInvalidLogSequence</p> | <p>Le jeu de fichiers journaux du jeu de sauvegarde et du chemin d’accès du journal actuel ne correspond pas.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. cette erreur est retournée par <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> lorsque le moteur est en mode multi-instance et pinstance fait référence à une instance non valide Windows XP et versions ultérieures.</p> | 
| <p>JET_errInvalidPath</p> | <p>L’opération a échoué, car certains chemins d’accès fournis ne sont pas valides (le chemin de sauvegarde, le chemin d’accès de destination, le journal ou le chemin d’accès du système pour l’instance).</p> | 
| <p>JET_errPageSizeMismatch</p> | <p>L’opération a échoué car le moteur est configuré pour utiliser une taille de page de base de données (à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> pour <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) qui ne correspond pas à la taille de page de la base de données utilisée pour créer les fichiers du journal des transactions ou les bases de données associées aux fichiers du journal des transactions.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>l’opération a échoué, car les paramètres impliquaient le mode d’instance unique (Windows mode de compatibilité 2000) et le moteur est déjà en mode multi-instance.</p> | 



En cas de réussite, les fichiers de base de données du jeu de sauvegarde sont restaurés dans leur emplacement et la récupération est exécutée de sorte que les bases de données se trouvent dans un état de cohérence des transactions propre. La récupération va relire les fichiers journaux du jeu de sauvegarde et les fichiers journaux du chemin d’accès du journal, si ces fichiers existent. Cette récupération entraîne des modifications du fichier de point de contrôle, des fichiers journaux des transactions et des bases de données référencées par ces fichiers journaux de transactions.

En cas d’échec, l’instance reste dans un État non initialisé. L’état des fichiers du journal des transactions et des bases de données référencées par ces fichiers du journal des transactions aura probablement été modifié lors de la tentative d’initialisation de la restauration et de récupération des bases de données.

#### <a name="remarks"></a>Remarques

Le processus de récupération reconstruira les bases de données attachées à l’instance au cours de la sauvegarde et enregistrera les modifications dans les fichiers de la base de données. Le résultat sera celui des bases de données qui sont cohérentes avec les transactions. Si possible, il enregistrera également dans la base de données les modifications apportées depuis la sauvegarde jusqu’à la dernière modification trouvée dans les journaux des transactions. Cela est possible si les journaux des transactions générés depuis la sauvegarde sont toujours présents dans le répertoire du journal des transactions. Notez que si la journalisation circulaire a été activée pour l’instance, les journaux de transactions générés sont réutilisés afin que la récupération puisse enregistrer les modifications apportées jusqu’à l’heure de la sauvegarde. Dans tous les cas, il est possible que ce processus prenne un certain temps si le nombre de fichiers du journal des transactions à relire sur les bases de données est important.

Les fonctions [JetRestore](./jetrestore-function.md) doivent être appelées sur une instance avant que [JetInit](./jetinit-function.md) soit appelé pour cette instance.

Étant donné que, lors de la récupération, un nombre important de pages de base de données et de journaux de transactions sera utilisé, il existe une série complète d’erreurs qui peuvent être renvoyées par ces fonctions. Ces erreurs peuvent provenir d’échecs d’allocation de ressources, comme Jet_errOutOfMemory aux erreurs qui représentent des altérations physiques comme JET_errReadVerifyFailure, JET_errLogFileCorrupt ou JET_errBadPageLink. Ces erreurs sont presque toujours dues à des problèmes matériels et ne peuvent donc pas être évitées. La gestion des fichiers se manifeste le plus souvent en tant que JET_errMissingLogFile ou JET_errAttachedDatabaseMismatch ou JET_errDatabaseSharingViolation ou JET_errInvalidLogSequence. Ces erreurs sont empêchables par l’application. L’application doit veiller à protéger le référentiel de ces fichiers contre les manipulations en dehors des forces, telles que l’utilisateur ou d’autres applications. Si l’application souhaite détruire entièrement une instance, tous les fichiers associés à l’instance doivent être supprimés. Celles-ci incluent le fichier de point de contrôle, les fichiers journaux des transactions et les fichiers de base de données attachés à l’instance.

Les différentes étapes de la récupération auront des entrées de journal des événements générées, notamment la progression de la relecture du journal des transactions et le résultat final de la restauration.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetRestore2W</strong> (Unicode) et <strong>JetRestore2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
