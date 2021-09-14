---
description: 'En savoir plus sur : fonction JetGetLogInfoInstance2'
title: JetGetLogInfoInstance2 fonction)
TOCTitle: JetGetLogInfoInstance2 Function
ms:assetid: 50fdae92-611c-4dbf-846e-86cc836a23db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269247(v=EXCHG.10)
ms:contentKeyID: 32765549
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance2W
- JetGetLogInfoInstance2
- JetGetLogInfoInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec8bf0a4cee4e89f8252e53ed0ffbeb3aed4bcdf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854157"
---
# <a name="jetgetloginfoinstance2-function"></a>JetGetLogInfoInstance2 fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetloginfoinstance2-function"></a>JetGetLogInfoInstance2 fonction)

La fonction **JetGetLogInfoInstance2** est utilisée lors d’une sauvegarde lancée par [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) pour interroger une instance pour obtenir les noms des fichiers de correctifs de base de données et des fichiers journaux des transactions qui doivent faire partie du jeu de fichiers de sauvegarde. Ces fichiers peuvent être ouverts par la suite à l’aide de [JetOpenFile](./jetopenfile-function.md) et lus à l’aide de [JetReadFile](./jetreadfile-function.md).

**Windows xp : JetGetLogInfoInstance2** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetGetLogInfoInstance2(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in_out_opt  JET_LOGINFO* pLogInfo
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance à utiliser pour cet appel.

pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge. L’utilisation de cette instance globale est implicitement dans ce cas.

pour Windows XP et versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (Windows mode de compatibilité 2000), où une seule instance est prise en charge. Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.

*szz*

Mémoire tampon de sortie qui recevra la liste des chaînes terminées par un caractère null qui décrivent l’ensemble des fichiers de correctifs de base de données et des fichiers journaux des transactions qui doivent faire partie du jeu de fichiers de sauvegarde.

La liste de chaînes retournée dans cette mémoire tampon est dans le même format qu’une chaîne multiple utilisée par le registre. Chaque chaîne se terminant par une valeur null est retournée dans la séquence suivie d’une marque de fin null finale.

*cbMax*

Taille maximale, en octets, de la mémoire tampon de sortie.

*pcbActual*

Reçoit le volume réel de données de chaîne reçues dans la mémoire tampon de sortie.

*pLogInfo*

Reçoit des informations structurées sur les fichiers du journal des transactions qui doivent faire partie du jeu de fichiers de sauvegarde.

Lorsque ce paramètre n’est pas présent, sa valeur est supposée être NULL.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>L’opération de sauvegarde a échoué, car elle était appelée hors séquence. <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> retourne cette erreur s’il existe des descripteurs de fichiers en attente créés à l’aide de <a href="gg269249(v=exchg.10).md">JetOpenFile</a> pour l’instance.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. cela peut se produire pour <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> lorsque le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</p> | 
| <p>JET_errNoBackup</p> | <p>L’opération a échoué, car aucune sauvegarde externe n’est en cours.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>l’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (Windows mode de compatibilité 2000), où une seule instance est prise en charge lorsqu’il existe déjà plusieurs instances.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, les informations demandées sur l’ensemble des fichiers de correctifs de base de données et les fichiers journaux des transactions qui doivent faire partie du jeu de fichiers de sauvegarde seront placées dans les tampons de sortie, le cas échéant. L’ordinateur d’état de sauvegarde est avancé, de sorte que la sauvegarde des fichiers de base de données n’est plus autorisée. Seuls les fichiers de correctifs de base de données et les fichiers journaux des transactions sont autorisés à être ouverts pour la sauvegarde au-delà de ce point.

En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini. L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance.

#### <a name="remarks"></a>Notes

Il est important de noter que cette API ne retourne pas d’erreur ou d’avertissement si la mémoire tampon de sortie est trop petite pour accepter la liste complète des fichiers qui doivent faire partie du jeu de fichiers de sauvegarde. L’application doit toujours fournir une mémoire tampon pour recevoir la taille réelle de cette liste et utiliser ces informations pour déterminer si la liste a été tronquée.

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetGetLogInfoInstance2W</strong> (Unicode) et <strong>JetGetLogInfoInstance2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)
