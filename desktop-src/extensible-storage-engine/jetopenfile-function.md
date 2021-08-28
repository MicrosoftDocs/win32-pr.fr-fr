---
description: 'En savoir plus sur : fonction JetOpenFile'
title: Fonction JetOpenFile
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffe4527390e21e86ed46820125eb2a422367d8ec
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480375"
---
# <a name="jetopenfile-function"></a>Fonction JetOpenFile


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetopenfile-function"></a>Fonction JetOpenFile

La fonction **JetOpenFile** ouvre une base de données attachée, un fichier de correctif de base de données ou un fichier journal de transactions d’une instance active afin d’effectuer une sauvegarde floue en continu. Les données de ces fichiers peuvent ensuite être lues par le handle retourné à l’aide de [JetReadFile](./jetreadfile-function.md). Le handle retourné doit être fermé à l’aide de [JetCloseFile](./jetclosefile-function.md). Une sauvegarde externe de l’instance doit avoir été précédemment lancée à l’aide de [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Paramètres

*szFileName*

Chemin relatif ou absolu d’une base de données attachée, d’un fichier de correctif de base de données ou d’un fichier journal de transactions géré par l’instance qui sera lue pour la sauvegarde.

*phfFile*

Mémoire tampon de sortie qui reçoit un handle vers le fichier à lire.

*pulFileSizeLow*

Mémoire tampon de sortie qui reçoit les 32 bits les moins significatifs de la taille du fichier.

*pulFileSizeHigh*

Mémoire tampon de sortie qui reçoit les 32 bits les plus significatifs de la taille du fichier.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errFileAccessDenied</p> | <p>L’opération a échoué car elle n’a pas pu ouvrir le fichier demandé en raison d’une violation de partage ou de privilèges insuffisants.</p> | 
| <p>JET_errFileNotFound</p> | <p>L’opération a échoué, car elle n’a pas pu ouvrir le fichier demandé, car il est introuvable dans le chemin d’accès spécifié. cette erreur est renvoyée uniquement par Windows 2000.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetOpenFile</strong> dans les cas suivants :</p><ul><li><p>le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</p></li><li><p>le paramètre de nom de fichier spécifié est NULL ou une chaîne de longueur nulle (Windows XP et versions ultérieures).</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>L’opération a échoué, car le chemin d’accès spécifié est introuvable.</p> | 
| <p>JET_errMissingFileToBackup</p> | <p>Le fichier demandé n’a pas pu être ouvert pour la sauvegarde, car il est introuvable. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errNoBackup</p> | <p>L’opération a échoué, car aucune sauvegarde externe n’est en cours.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L’opération a échoué, car la mémoire peut être allouée pour être terminée. <strong>JetOpenFile</strong> retourne JET_errOutOfMemory si une tentative est faite pour ouvrir un autre fichier avant que le fichier précédent ouvert à l’aide de <strong>JetOpenFile</strong> ait été fermé par <a href="gg294127(v=exchg.10).md">JetCloseFile</a>. Un seul descripteur de fichier en attente est actuellement pris en charge.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>l’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (Windows mode de compatibilité 2000), où une seule instance est prise en charge lorsqu’il existe déjà plusieurs instances.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt. JET_errRestoreInProgress il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 



En cas de réussite, un handle vers le fichier demandé est retourné. Si le descripteur concerne un fichier de base de données, ce fichier de base de données sera préparé pour la sauvegarde en continu, ce qui peut entraîner la création d’un fichier correctif de base de données au même emplacement que le fichier de base de données. Le fichier de correctif de base de données a exactement le même chemin d’accès et le même nom de fichier que le fichier de base de données, mais il a un. Extension PAT. La taille du fichier est également retournée.

En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini. Un fichier de correctif de base de données peut être créé temporairement sur le disque et tout fichier existant à l’emplacement du fichier correctif peut être supprimé. L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance. dans Windows XP et les versions ultérieures, la sauvegarde n’est pas annulée si une tentative de sauvegarde d’une base de données qui n’était pas attachée à l’instance a été effectuée au moment de l’appel.

**Avertissement**  Pour des raisons de sécurité, il est important de noter que **JetOpenFile** ne vérifie pas que le chemin de fichier demandé est associé à l’ensemble des fichiers qui doivent être sauvegardés pour l’instance. Par conséquent, il est possible d’utiliser cette fonction pour accéder à n’importe quel fichier pouvant être ouvert par le contexte de sécurité actuel du thread. Il est impératif que l’application limite les chemins passés à cette fonction à un ensemble connu de chemins d’accès de fichier corrects, ou qu’une divulgation d’informations puisse être rendue possible.

#### <a name="remarks"></a>Remarques

Les mémoires tampons de sortie du handle et de la taille du fichier doivent être présentes. Si elles ne sont pas présentes, le moteur se bloque car les paramètres de mémoire tampon de sortie ne sont pas validés.

À ce stade, un seul fichier peut être ouvert à la sauvegarde à un moment donné.

**JetOpenFile** ne déclare pas le privilège de sauvegarde avant l’ouverture du fichier demandé.

La taille du fichier à lire comme indiqué par cette fonction peut ne pas correspondre à la taille du fichier sur le disque. sur Windows XP et les versions ultérieures, des informations supplémentaires peuvent être ajoutées à un fichier de base de données qui est utilisé par le moteur de base de données lors d’une opération de restauration. Par conséquent, l’application doit uniquement s’appuyer sur la taille de fichier retournée par **JetOpenFile** ou sur le nombre réel d’octets de données retournés par [JetReadFile](./jetreadfile-function.md).

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetOpenFileW</strong> (Unicode) et <strong>JetOpenFileA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
