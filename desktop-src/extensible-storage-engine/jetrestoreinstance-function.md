---
description: 'En savoir plus sur : fonction JetRestoreInstance'
title: Fonction JetRestoreInstance
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 638ec789417dcd35e63758263227245f6c22d65b3c7bb7dff775420c0bac2d66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978849"
---
# <a name="jetrestoreinstance-function"></a>Fonction JetRestoreInstance


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetrestoreinstance-function"></a>Fonction JetRestoreInstance

La fonction **JetRestoreInstance** restaure et récupère une sauvegarde en continu d’une instance, y compris toutes les bases de données attachées. Il est conçu pour fonctionner avec une sauvegarde créée avec la fonction [JetBackupInstance](./jetbackupinstance-function.md) . Il s’agit de la fonction de restauration la plus simple et la plus encapsulée.

**Windows xp :****JetRestoreInstance** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Spécifie l’instance à utiliser pour cet appel.

pour Windows XP et versions ultérieures, l’utilisation de ce paramètre dépend du mode de fonctionnement du moteur. si le moteur fonctionne en mode hérité (Windows mode de compatibilité 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la valeur null ou il peut être défini sur une mémoire tampon de sortie valide contenant la valeur null ou JET_instanceNil qui retournera le handle d’instance global créé comme un effet secondaire de l’initialisation. Ce descripteur d’instance peut ensuite être passé à toute autre API qui prend une instance. Si le moteur fonctionne en mode multi-instance, ce paramètre doit être défini sur une mémoire tampon d’entrée valide qui contient le handle d’instance retourné par [JetCreateInstance](./jetcreateinstance-function.md) qui est en cours d’initialisation.

*SZ*

Dossier dans lequel se trouve la sauvegarde. La sauvegarde doit avoir été générée à l’aide des API [JetBackup](./jetbackup-function.md) .

*szDest*

Nom du dossier dans lequel les fichiers de base de données du jeu de sauvegarde seront copiés et récupérés. Si la valeur est NULL (ce qui est le cas pour le [JetRestore](./jetrestore-function.md)hérité), les fichiers de base de données sont copiés et récupérés à leur emplacement d’origine.

*PFN*

Pointeur facultatif vers la fonction qui sera appelée en tant qu’informations de notification sur la progression de l’opération de restauration.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>L’opération a échoué, car le moteur est déjà initialisé pour cette instance.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLogSequence</p></td>
<td><p>Le jeu de fichiers journaux du jeu de sauvegarde et du chemin d’accès du journal actuel ne correspond pas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. cette erreur est retournée par <strong>JetRestoreInstance</strong> lorsque le moteur est en mode multi-instance et pinstance fait référence à une instance non valide Windows XP et versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>L’opération a échoué, car certains chemins d’accès fournis ne sont pas valides (le chemin de sauvegarde, le chemin d’accès de destination, le journal ou le chemin d’accès du système pour l’instance).</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch</p></td>
<td><p>L’opération a échoué car le moteur est configuré pour utiliser une taille de page de base de données (à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> pour <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) qui ne correspond pas à la taille de page de la base de données utilisée pour créer les fichiers du journal des transactions ou les bases de données associées aux fichiers du journal des transactions.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>l’opération a échoué, car les paramètres impliquaient le mode d’instance unique (Windows mode de compatibilité 2000) et le moteur est déjà en mode multi-instance.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, les fichiers de base de données du jeu de sauvegarde sont restaurés dans leur emplacement et la récupération est exécutée de sorte que les bases de données se trouvent dans un état de cohérence des transactions propre. La récupération va relire les fichiers journaux du jeu de sauvegarde et les fichiers journaux du chemin d’accès du journal, si ces fichiers existent. Cette récupération entraîne des modifications du fichier de point de contrôle, des fichiers journaux des transactions et des bases de données référencées par ces fichiers journaux de transactions.

En cas d’échec, l’instance reste dans un État non initialisé. L’état des fichiers du journal des transactions et des bases de données référencées par ces fichiers du journal des transactions aura probablement été modifié lors de la tentative d’initialisation de la restauration et de récupération des bases de données.

#### <a name="remarks"></a>Remarques

Le processus de récupération reconstruira les bases de données attachées à l’instance au cours de la sauvegarde et enregistrera les modifications dans les fichiers de la base de données. Le résultat sera celui des bases de données qui sont cohérentes avec les transactions. Si possible, il enregistrera également dans la base de données les modifications apportées depuis la sauvegarde jusqu’à la dernière modification trouvée dans les journaux des transactions. Cela est possible si les journaux des transactions générés depuis la sauvegarde sont toujours présents dans le répertoire du journal des transactions. Notez que si la journalisation circulaire a été activée pour l’instance, les journaux de transactions générés sont réutilisés afin que la récupération puisse enregistrer les modifications apportées jusqu’à l’heure de la sauvegarde. Dans tous les cas, il est possible que ce processus prenne un certain temps si le nombre de fichiers du journal des transactions à relire sur les bases de données est important.

**JetRestoreInstance** doit être appelé sur une instance qui a déjà été créée à l’aide de [JetCreateInstance](./jetcreateinstance-function.md).

Étant donné que, lors de la récupération, un nombre important de pages de base de données et de journaux de transactions sera utilisé, il existe une série complète d’erreurs qui peuvent être renvoyées par ces fonctions. Ces erreurs peuvent provenir d’échecs d’allocation de ressources, comme Jet_errOutOfMemory aux erreurs qui représentent des altérations physiques comme JET_errReadVerifyFailure, JET_errLogFileCorrupt ou JET_errBadPageLink. Ces erreurs sont presque toujours dues à des problèmes matériels et ne peuvent donc pas être évitées. La gestion des fichiers se manifeste le plus souvent en tant que JET_errMissingLogFile ou JET_errAttachedDatabaseMismatch ou JET_errDatabaseSharingViolation ou JET_errInvalidLogSequence. Ces erreurs sont empêchables par l’application. L’application doit veiller à protéger le référentiel de ces fichiers contre les manipulations en dehors des forces, telles que l’utilisateur ou d’autres applications. Si l’application souhaite détruire entièrement une instance, tous les fichiers associés à l’instance doivent être supprimés. Celles-ci incluent le fichier de point de contrôle, les fichiers journaux des transactions et les fichiers de base de données attachés à l’instance.

Les différentes étapes de la récupération auront des entrées de journal des événements générées, notamment la progression de la relecture du journal des transactions et le résultat final de la restauration.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>requiert Windows server 2008 ou Windows server 2003.</p></td>
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
<td><p>Implémenté en tant que <strong>JetRestoreInstanceW</strong> (Unicode) et <strong>JetRestoreInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
