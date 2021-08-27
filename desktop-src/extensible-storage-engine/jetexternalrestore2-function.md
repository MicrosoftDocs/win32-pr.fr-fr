---
description: 'En savoir plus sur : fonction JetExternalRestore2'
title: Fonction JetExternalRestore2
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad8cad0cfc31c77b3cc8e960153bda14b4f431e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475815"
---
# <a name="jetexternalrestore2-function"></a>Fonction JetExternalRestore2


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetexternalrestore2-function"></a>Fonction JetExternalRestore2

La fonction **JetExternalRestore2** restaure une sauvegarde externe qui a été effectuée avec les API de sauvegarde externes et fournit des points de contrôle à utiliser pour les opérations de journalisation circulaire. C’est ce que l’on appelle la récupération matérielle, qui est similaire, mais différente de la récupération logicielle, telle qu’elle est exécutée par la fonction [JetInit](./jetinit-function.md) .

**Windows xp : JetExternalRestore2** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Paramètres

*szCheckpointFilePath*

Chemin d’accès pour le fichier de point de contrôle à utiliser pendant la récupération si *szTargetInstanceCheckpointPath* n’est pas spécifié ou si le chemin d’accès a une instance active ou en cours d’exécution.

*szLogPath*

Chemin d’accès ou répertoire des journaux pour la phase finale (annulation) de la récupération et éventuellement pour les journaux de restauration par progression. Ce chemin d’accès peut être le même que le *szBackupLogPath*.

*rgrstmap*

Il s’agit d’un tableau de structures [JET_RSTMAP](./jet-rstmap-structure.md) . Il s’agit d’une table de chemins d’accès ou de noms de fichiers anciens et nouveaux. Cela est utilisé, car les bases de données peuvent devoir être récupérées dans un emplacement autre que l’emplacement à partir duquel elles ont été sauvegardées. Dans le cas où plusieurs bases de données sont attachées à un seul jeu de journalisation, le mappage de restauration peut spécifier un sous-ensemble des bases de données à restaurer.

*crstfilemap*

Nombre d’entrées dans le paramètre de tableau *rgrstmap* .

*szBackupLogPath*

Chemin d’accès au répertoire dans lequel les fichiers journaux sont restaurés. Il s’agit des journaux qui ont été lus pendant la séquence de sauvegarde externe. Ce chemin d’accès peut être le même que le *szLogPath*.

*pLogInfo*

Le *pLogInfo* décrit plusieurs aspects des journaux de sauvegarde à récupérer. ce paramètre permet à **JetExternalRestore2** de prendre les paramètres *genLow* et *genHigh* explicites que **JetExternalRestore2** a, ainsi que le nom du journal de base, au lieu d’un nom de base de journal présumé « edb ».

*szTargetInstanceName*

Ce paramètre est déconseillé et ne peut pas être utilisé dans votre application.

*szTargetInstanceLogPath*

Le chemin d’accès pour les journaux de restauration par progression si l’emplacement des journaux que vous souhaitez restaurer par progression se trouve dans un ensemble ou une instance de journalisation active. Cela ne doit pas être spécifié si l’instance cible utilise la journalisation circulaire.

*szTargetInstanceCheckpointPath*

Chemin d’accès du point de contrôle pendant la récupération si aucune instance active n’est en cours d’exécution sur cette cible. Cela ne doit pas être spécifié si l’instance cible utilise la journalisation circulaire.

*PFN*

Rappel d’État qui indique la progression de la récupération.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBadRestoreTargetInstance</p> | <p>Le <em>szTargetInstanceLogPath</em> spécifié n’appartient pas à une instance initialisée. cette erreur est renvoyée uniquement dans Windows XP et versions ultérieures.</p> | 
| <p>JET_errDatabaseCorrupted</p> | <p>Cela indique que la base de données a été endommagée ou un fichier non reconnu.</p> | 
| <p>JET_errEndingRestoreLogTooLow</p> | <p>Cette erreur est retournée si l’une des fichiers journaux dans le <em>szBackupLogPath</em>a une génération de journal supérieure à celle spécifiée dans <em>genHigh</em> ou <em>pLogInfo. ulGenHigh</em>.</p> | 
| <p>JET_errFileNotFound</p> | <p>L’opération a échoué, car elle n’a pas pu ouvrir le fichier demandé, car il est introuvable dans le chemin d’accès spécifié.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, et ainsi de suite lorsque le <em>SzTargetCheckpointPath</em> et le <em>szTargetInstanceLogPath</em> ne sont pas tous les deux spécifiés ou non spécifiés. Autrement dit, ils doivent correspondre et être spécifiés ou non spécifiés.</p> | 
| <p>JET_errInvalidPath</p> | <p>L’opération a échoué, car le chemin d’accès spécifié est introuvable.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L’opération a échoué, car la mémoire peut être allouée pour être terminée.</p> | 
| <p>JET_errRestoreOfNonBackupDatabase</p> | <p>Cette erreur est retournée si le fichier de base de données spécifié lors de la restauration n’est pas une base de données qui a été sauvegardée avec une sauvegarde externe.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Le moteur de base de données ne peut pas exécuter une restauration externe ou une récupération matérielle en mode instance unique. cette erreur est renvoyée uniquement dans Windows XP et versions ultérieures.</p> | 
| <p>JET_errStartingRestoreLogTooHigh</p> | <p>Cette erreur est retournée si l’un des fichiers journaux dans <em>szBackupLogPath</em>a une génération de journal ci-dessous, spécifiée par <em>genLow</em> ou <em>pLogInfo. ulGenLow</em>.</p> | 



En cas de réussite, toutes les bases de données du *rgrstmap* sont entièrement récupérées et dans un état propre ou cohérent. À ce stade, la base de données peut être remontée sur une instance existante.

En cas d’échec, le moteur n’a pas pu récupérer la base de données. La base de données est dans un État non valide et, afin de retenter la récupération matérielle, la base de données entière doit être restaurée à nouveau. En règle générale, la source d’une telle situation est l’endommagement du disque ou du journal, ou une autre forme de gestion des journaux ou un ensemble de journaux non continus.

#### <a name="remarks"></a>Remarques

Consultez [JetExternalRestore](./jetexternalrestore-function.md).

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetExternalRestore2W</strong> (Unicode) et <strong>JetExternalRestore2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
