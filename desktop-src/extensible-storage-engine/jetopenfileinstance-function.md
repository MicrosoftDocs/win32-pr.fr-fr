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
ms.openlocfilehash: 6065914fcd5b03d8c8b05996d57331a474ad7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523067"
---
# <a name="jetopenfileinstance-function"></a>Fonction JetOpenFileInstance


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetopenfileinstance-function"></a>Fonction JetOpenFileInstance

La fonction **JetOpenFileInstance** ouvre une base de données attachée, un fichier de correctif de base de données ou un fichier journal de transactions d’une instance active afin d’effectuer une sauvegarde floue en continu. Les données de ces fichiers peuvent ensuite être lues par le handle retourné à l’aide de [JetReadFileInstance](./jetreadfileinstance-function.md). Le handle retourné doit être fermé à l’aide de [JetCloseFileInstance](./jetclosefileinstance-function.md). Une sauvegarde externe de l’instance doit avoir été précédemment lancée à l’aide de [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).

**Windows XP :**  **JetOpenFileInstance** est introduit dans Windows XP.

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

Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge. L’utilisation de cette instance globale est implicitement dans ce cas.

Pour Windows XP et les versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) alors qu’une seule instance est prise en charge. Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.

*szFileName*

Chemin relatif ou absolu d’une base de données attachée, d’un fichier de correctif de base de données ou d’un fichier journal de transactions géré par l’instance en lecture pour la sauvegarde.

*phfFile*

Pointeur vers la mémoire tampon de sortie qui reçoit un handle vers le fichier à lire.

*pulFileSizeLow*

Pointeur vers la mémoire tampon de sortie qui reçoit les 32 bits les moins significatifs de la taille du fichier.

*pulFileSizeHigh*

Pointeur vers la mémoire tampon de sortie qui reçoit les 32 bits les plus significatifs de la taille du fichier.

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
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>L’opération a échoué car elle n’a pas pu ouvrir le fichier demandé en raison d’une violation de partage ou de privilèges insuffisants.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>L’opération a échoué, car elle n’a pas pu ouvrir le fichier demandé, car il est introuvable dans le chemin d’accès spécifié. Cette erreur est renvoyée uniquement par Windows 2000.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>L’opération a échoué, car le chemin d’accès spécifié est introuvable.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetOpenFileInstance</strong> dans les cas suivants :</p>
<ul>
<li><p>Le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</p></li>
<li><p>Le paramètre de nom de fichier spécifié est NULL ou une chaîne de longueur nulle (Windows XP et versions ultérieures).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFileToBackup</p></td>
<td><p>Le fichier demandé n’a pas pu être ouvert pour la sauvegarde, car il est introuvable. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>L’opération a échoué, car aucune sauvegarde externe n’est en cours.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L’opération a échoué, car la mémoire peut être allouée pour être terminée. <strong>JetOpenFileInstance</strong> retourne JET_errOutOfMemory si une tentative est faite pour ouvrir un autre fichier avant que le fichier précédent ouvert à l’aide de <strong>JetOpenFileInstance</strong> ait été fermé par <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>. Un seul descripteur de fichier en attente est actuellement pris en charge.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, un handle vers le fichier demandé est retourné. Si le descripteur concerne un fichier de base de données, ce fichier de base de données sera préparé pour une sauvegarde en continu, ce qui peut entraîner la création d’un fichier correctif de base de données au même emplacement que le fichier de base de données. Le fichier de correctif de base de données a exactement le même chemin d’accès et le même nom de fichier que le fichier de base de données, mais avec un. Extension PAT. La taille du fichier est également retournée.

En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini. Un fichier de correctif de base de données peut être créé temporairement sur le disque et tout fichier existant à l’emplacement du fichier correctif peut être supprimé. L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance. Sur Windows XP et versions ultérieures, la sauvegarde n’est pas annulée si une tentative de sauvegarde d’une base de données n’a pas été attachée à l’instance au moment de l’appel a été effectuée.

**Avertissement**  Pour des raisons de sécurité, il est important de noter que **JetOpenFileInstance** ne vérifie pas que le chemin de fichier demandé est associé à l’ensemble des fichiers sauvegardés pour l’instance. Par conséquent, il est possible d’utiliser cette fonction pour accéder à n’importe quel fichier pouvant être ouvert par le contexte de sécurité actuel du thread. Il est impératif que l’application limite les chemins passés à cette fonction à un ensemble connu de chemins d’accès de fichier corrects, ou qu’une divulgation d’informations puisse être rendue possible.

#### <a name="remarks"></a>Notes

Les mémoires tampons de sortie du handle et de la taille du fichier doivent être présentes. Si elles ne sont pas présentes, le moteur se bloque car les paramètres de mémoire tampon de sortie ne sont pas validés.

À ce stade, un seul fichier peut être ouvert à la sauvegarde à un moment donné.

**JetOpenFileInstance** ne déclare pas le privilège de sauvegarde avant l’ouverture du fichier demandé.

La taille du fichier à lire comme indiqué par cette fonction peut ne pas correspondre à la taille du fichier sur le disque. Sur Windows XP et versions ultérieures, des informations supplémentaires peuvent être ajoutées à un fichier de base de données qui est utilisé par le moteur de base de données lors d’une opération de restauration. Par conséquent, l’application doit uniquement s’appuyer sur la taille de fichier retournée par **JetOpenFileInstance** ou sur le nombre réel d’octets de données retournés par [JetReadFileInstance](./jetreadfileinstance-function.md).

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
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
<td><p>Implémenté en tant que <strong>JetOpenFileInstanceW</strong> (Unicode) et <strong>JetOpenFileInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
