---
description: 'En savoir plus sur : fonction JetExternalRestore'
title: JetExternalRestore fonction)
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106542207"
---
# <a name="jetexternalrestore-function"></a>JetExternalRestore fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetexternalrestore-function"></a>JetExternalRestore fonction)

La fonction **JetExternalRestore** restaure une sauvegarde externe qui a été effectuée avec les API de sauvegarde externes et spécifie une plage de numéros de fichier journal à relire pendant le processus de restauration. C’est ce que l’on appelle la récupération matérielle, qui est semblable à mais différente de la récupération logicielle telle qu’elle est exécutée par la fonction [JetInit](./jetinit-function.md) .

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a>Paramètres

*szCheckpointFilePath*

Chemin d’accès du fichier de point de contrôle à utiliser pendant la récupération si *szTargetInstanceCheckpointPath* n’est pas spécifié ou s’il dispose déjà d’une instance active ou en cours d’exécution.

*szLogPath*

Chemin d’accès ou répertoire des journaux pour la phase finale (annulation) de la récupération et éventuellement pour les journaux de restauration par progression. Ce chemin d’accès peut être le même que le *szBackupLogPath*.

*rgrstmap*

Il s’agit d’un tableau de structures [JET_RSTMAP](./jet-rstmap-structure.md) . Il s’agit d’une table de chemins d’accès ou de noms de fichiers anciens et nouveaux. Cela est utilisé, car les bases de données peuvent devoir être récupérées dans un emplacement autre que l’emplacement à partir duquel elles ont été sauvegardées. Dans le cas où plusieurs bases de données sont attachées à un seul jeu de journalisation, le mappage de restauration peut spécifier un sous-ensemble de bases de données à restaurer.

*crstfilemap*

Nombre d’entrées dans le paramètre de tableau *rgrstmap* .

*szBackupLogPath*

Chemin d’accès au répertoire dans lequel les fichiers journaux sont restaurés. Il s’agit des journaux qui ont été lus pendant la séquence de sauvegarde externe. Ce chemin d’accès peut être le même que le szLogPath.

*genLow*

Numéro de fichier journal le plus bas à relire à partir de *szBackupLogPath*. La fidélité complète d’un long non signé doit être conservée, mais dans les versions actuelles du moteur, ce nombre est un nombre hexadécimal compris entre 0x00000 et 0xFFFFF. Cela peut changer dans les versions ultérieures.

*genHigh*

Numéro de fichier journal le plus élevé à relire à partir de *szBackupLogPath*. La fidélité complète d’un long non signé doit être conservée, mais dans les versions actuelles du moteur, ce nombre est un nombre hexadécimal compris entre 0x00000 et 0xFFFFF. Cela peut changer dans les versions ultérieures.

*PFN*

Rappel d’État pour signaler la progression de la récupération.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>L’opération a échoué, car la mémoire peut être allouée pour être terminée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetExternalRestore</strong>, et ainsi de suite lorsque le <em>SzTargetCheckpointPath</em> et le <em>szTargetInstanceLogPath</em> ne sont pas tous les deux spécifiés ou non spécifiés. Autrement dit, ils doivent correspondre et être spécifiés ou non spécifiés.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Cela indique que la base de données a été endommagée ou un fichier non reconnu.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>L’opération a échoué, car elle n’a pas pu ouvrir le fichier demandé, car il est introuvable dans le chemin d’accès spécifié.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>L’opération a échoué, car le chemin d’accès spécifié est introuvable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Cette erreur est retournée si le fichier de base de données spécifié lors de la restauration n’est pas une base de données qui a été sauvegardée avec une sauvegarde externe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Cette erreur est retournée si l’un des fichiers journaux dans <em>szBackupLogPath</em>a une génération de journal ci-dessous, spécifiée par <em>genLow</em> ou <em>pLogInfo. ulGenLow</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Cette erreur est retournée si l’un des fichiers journaux dans le <em>szBackupLogPath</em>a une génération de journal supérieure à celle spécifiée dans <em>genHigh</em> ou <em>pLogInfo. ulGenHigh</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>Le <em>szTargetInstanceLogPath</em> spécifié n’appartient pas à une instance initialisée. Cette erreur est renvoyée uniquement dans Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Le moteur de base de données ne peut pas exécuter une restauration externe ou une récupération matérielle en mode instance unique. Cette erreur est renvoyée uniquement dans Windows XP et les versions ultérieures.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, toutes les bases de données du *rgrstmap* sont entièrement récupérées et dans un état propre ou cohérent. À ce stade, la base de données peut être remontée sur une instance existante.

En cas d’échec, le moteur n’a pas pu récupérer la base de données. La base de données est dans un État non valide et, afin de retenter la récupération matérielle, la base de données entière doit être restaurée à nouveau. En règle générale, la source d’une telle situation est l’endommagement du disque ou du journal, ou une autre forme de gestion des journaux ou un ensemble de journaux non continus.

#### <a name="remarks"></a>Notes

Pour comprendre le fonctionnement d’une récupération « dure », vous devez comprendre qu’il existe trois phases de récupération et que la deuxième phase peut avoir deux parties. Dans la phase I, les journaux sont requis pour ramener une base de données sauvegardée à la cohérence (ou un ensemble initial de journaux incrémentiels peut être utilisé). Au cours de la phase II, tous les journaux de restauration par progression supplémentaires disponibles sont utilisés pour rendre la base de données cohérente. Il y a également une relecture des journaux de restauration par progression supplémentaires. La phase III est la phase d’annulation de la récupération.

Phase I : la relecture de l’ensemble des journaux qui doivent être restaurés pour que la base de données soit placée dans un état cohérent (ou un ensemble initial de fichiers journaux) est exécutée. Fondamentalement, il s’agit de la relecture de l’ensemble des fichiers journaux qui ne sont pas facultatifs pour les bases de données en cours de restauration. S’il manque des journaux dans cette plage de journaux, la restauration échoue. Ces journaux doivent être placés dans le répertoire spécifié dans le paramètre *szBackupLogPath* .

Phase II : éventuellement, il peut y avoir certains ensembles de fichiers journaux qui sont des fichiers journaux de restauration par progression issus de sauvegardes incrémentielles ou différentielles et des fichiers journaux d’une instance active. Dans le cas de fichiers journaux issus de sauvegardes incrémentielles ou différentielles, les fichiers journaux peuvent être placés dans les répertoires spécifiés dans les paramètres *szBackupLogPath* ou *szTargetInstanceLogPath* , l’ancien étant le répertoire recommandé. Les journaux utilisés pour la phase de restauration par progression (phase II) doivent provenir de la même série de journaux joués au cours de la phase I et doivent incrémenter continuellement les numéros de journal sans aucun écart par rapport à la phase I. Pour qu’une base de données soit entièrement à jour avec les fichiers journaux en cours d’utilisation par une instance active, les paramètres *szTargetInstanceLogPath* et *szTargetInstanceCheckpointPath* doivent être spécifiés. Cela peut être fait même si d’autres bases de données sont attachées à ce jeu de journaux.

Phase III : dans la dernière phase de la récupération, toutes les transactions non validées sont restaurées, ce qui nécessite la génération de nouveaux fichiers journaux et la mise à jour du fichier de point de contrôle. Cette phase est parfois appelée « annulation ». Le chemin d’accès au fichier de point de contrôle à utiliser au cours de cette phase est le chemin d’accès analogue à l’emplacement du journal de la phase III, autrement dit, si *szLogPath* est utilisé pour la phase III, *szCheckpointFilePath* sera utilisé, si *szTargetInstanceLogPath* est utilisé pour la phase III de la récupération *szTargetInstanceCheckpointPath* sera utilisé.

Pour comprendre le fonctionnement des tracés, utilisez cet organigramme :

![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")

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
<td><p>Implémenté en tant que <strong>JetExternalRestoreW</strong> (Unicode) et <strong>JetExternalRestoreA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetInit](./jetinit-function.md)
