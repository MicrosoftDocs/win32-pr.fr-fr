---
description: 'En savoir plus sur : fonction JetOpenFileInstance'
title: Fonction JetOpenFileInstance
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba66545c65abcaa3d3969ec7c3d61d73c57be732
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983372"
---
# <a name="jetopenfileinstance-function"></a>Fonction JetOpenFileInstance


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetopenfileinstance-function"></a>Fonction JetOpenFileInstance

La fonction **JetOpenFileInstance** ouvre une base de données attachée, un fichier de correctif de base de données ou un fichier journal de transactions d’une instance active afin d’effectuer une sauvegarde floue en continu. Les données de ces fichiers peuvent ensuite être lues par le handle retourné à l’aide de [JetReadFileInstance](./jetreadfileinstance-function.md). Le handle retourné doit être fermé à l’aide de [JetCloseFileInstance](./jetclosefileinstance-function.md). Une sauvegarde externe de l’instance doit avoir été précédemment lancée à l’aide de [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).

**Windows xp :****JetOpenFileInstance** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance à utiliser pour cet appel.

pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge. L’utilisation de cette instance globale est implicitement dans ce cas.

pour Windows XP et versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (Windows mode de compatibilité 2000), où une seule instance est prise en charge. Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.

*szFileName*

Chemin relatif ou absolu d’une base de données attachée, d’un fichier de correctif de base de données ou d’un fichier journal de transactions géré par l’instance en lecture pour la sauvegarde.

*phfFile*

Pointeur vers la mémoire tampon de sortie qui reçoit un handle vers le fichier à lire.

*pulFileSizeLow*

Pointeur vers la mémoire tampon de sortie qui reçoit les 32 bits les moins significatifs de la taille du fichier.

*pulFileSizeHigh*

Pointeur vers la mémoire tampon de sortie qui reçoit les 32 bits les plus significatifs de la taille du fichier.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p> | 
| <p>JET_errFileAccessDenied</p> | <p>L’opération a échoué car elle n’a pas pu ouvrir le fichier demandé en raison d’une violation de partage ou de privilèges insuffisants.</p> | 
| <p>JET_errFileNotFound</p> | <p>L’opération a échoué, car elle n’a pas pu ouvrir le fichier demandé, car il est introuvable dans le chemin d’accès spécifié. cette erreur est renvoyée uniquement par Windows 2000.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</p> | 
| <p>JET_errInvalidPath</p> | <p>L’opération a échoué, car le chemin d’accès spécifié est introuvable.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetOpenFileInstance</strong> dans les cas suivants :</p><ul><li><p>le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</p></li><li><p>le paramètre de nom de fichier spécifié est NULL ou une chaîne de longueur nulle (Windows XP et versions ultérieures).</p></li></ul> | 
| <p>JET_errMissingFileToBackup</p> | <p>Le fichier demandé n’a pas pu être ouvert pour la sauvegarde, car il est introuvable. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errNoBackup</p> | <p>L’opération a échoué, car aucune sauvegarde externe n’est en cours.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L’opération a échoué, car la mémoire peut être allouée pour être terminée. <strong>JetOpenFileInstance</strong> retourne JET_errOutOfMemory si une tentative est faite pour ouvrir un autre fichier avant que le fichier précédent ouvert à l’aide de <strong>JetOpenFileInstance</strong> ait été fermé par <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>. Un seul descripteur de fichier en attente est actuellement pris en charge.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>l’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (Windows mode de compatibilité 2000), où une seule instance est prise en charge lorsqu’il existe déjà plusieurs instances.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, un handle vers le fichier demandé est retourné. Si le descripteur concerne un fichier de base de données, ce fichier de base de données sera préparé pour une sauvegarde en continu, ce qui peut entraîner la création d’un fichier correctif de base de données au même emplacement que le fichier de base de données. Le fichier de correctif de base de données a exactement le même chemin d’accès et le même nom de fichier que le fichier de base de données, mais avec un. Extension PAT. La taille du fichier est également retournée.

En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini. Un fichier de correctif de base de données peut être créé temporairement sur le disque et tout fichier existant à l’emplacement du fichier correctif peut être supprimé. L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance. dans Windows XP et les versions ultérieures, la sauvegarde n’est pas annulée si une tentative de sauvegarde d’une base de données qui n’était pas attachée à l’instance a été effectuée au moment de l’appel.

**Avertissement**  Pour des raisons de sécurité, il est important de noter que **JetOpenFileInstance** ne vérifie pas que le chemin de fichier demandé est associé à l’ensemble des fichiers sauvegardés pour l’instance. Par conséquent, il est possible d’utiliser cette fonction pour accéder à n’importe quel fichier pouvant être ouvert par le contexte de sécurité actuel du thread. Il est impératif que l’application limite les chemins passés à cette fonction à un ensemble connu de chemins d’accès de fichier corrects, ou qu’une divulgation d’informations puisse être rendue possible.

#### <a name="remarks"></a>Remarques

Les mémoires tampons de sortie du handle et de la taille du fichier doivent être présentes. Si elles ne sont pas présentes, le moteur se bloque car les paramètres de mémoire tampon de sortie ne sont pas validés.

À ce stade, un seul fichier peut être ouvert à la sauvegarde à un moment donné.

**JetOpenFileInstance** ne déclare pas le privilège de sauvegarde avant l’ouverture du fichier demandé.

La taille du fichier à lire comme indiqué par cette fonction peut ne pas correspondre à la taille du fichier sur le disque. sur Windows XP et les versions ultérieures, des informations supplémentaires peuvent être ajoutées à un fichier de base de données qui est utilisé par le moteur de base de données lors d’une opération de restauration. Par conséquent, l’application doit uniquement s’appuyer sur la taille de fichier retournée par **JetOpenFileInstance** ou sur le nombre réel d’octets de données retournés par [JetReadFileInstance](./jetreadfileinstance-function.md).

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetOpenFileInstanceW</strong> (Unicode) et <strong>JetOpenFileInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFileInstance](./jetclosefileinstance-function.md)  
[JetGetAttachInfoInstance](./jetgetattachinfoinstance-function.md)  
[JetGetLogInfoInstance](./jetgetloginfoinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopBackupInstance](./jetstopbackupinstance-function.md)  
[JetTruncateLogInstance](./jettruncateloginstance-function.md)
