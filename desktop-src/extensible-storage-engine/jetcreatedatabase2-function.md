---
description: 'En savoir plus sur : fonction JetCreateDatabase2'
title: Fonction JetCreateDatabase2
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370f88f95a2eb8217dc06124b50c9ed165eb679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521904"
---
# <a name="jetcreatedatabase2-function"></a>Fonction JetCreateDatabase2


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetcreatedatabase2-function"></a>Fonction JetCreateDatabase2

La fonction **JetCreateDatabase2** crée et attache un fichier de base de données à utiliser avec le moteur de base de données ESE avec une taille de base de données maximale spécifiée. L’appel de **JetCreateDatabase2** avec *cpgDatabaseSizeMax* défini à zéro est identique à l’appel de [JETCREATEDATABASE](./jetcreatedatabase-function.md) avec *szConnect* défini sur null. Il est actuellement possible de créer jusqu’à sept bases de données par instance.

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*szFilename*

Nom de la base de données à créer.

*cpgDatabaseSizeMax*

Taille maximale, en pages de base de données, pour la base de données. La taille de page de la base de données par défaut est de 4 kilo-octets et peut être modifiée avec [JetSetSystemParameter](./jetsetsystemparameter-function.md) avant de créer une base de données.

Le fait de passer la valeur zéro signifie qu’il n’y a pas de valeur maximale appliquée par le moteur de base de données.

*pdbid*

Pointeur vers une mémoire tampon qui, sur un appel réussi, contient l’identificateur de la base de données. En cas d’échec, la valeur n’est pas définie.

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
<td><p>JET_bitDbOverwriteExisting</p></td>
<td><p>Par défaut, si <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> ou <strong>JetCreateDatabase2</strong> est appelé et que la base de données existe déjà, l’appel d’API échoue et la base de données d’origine n’est pas remplacée. JET_bitDbOverwriteExisting modifie ce comportement et l’ancienne base de données sera remplacée par une nouvelle. Windows XP et versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbRecoveryOff</p></td>
<td><p>JET_bitDbRecoveryOff désactive la journalisation. La définition de ce bit perd la possibilité de relire les fichiers journaux et de récupérer la base de données à un État utilisable cohérent après un événement catastrophique.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbShadowingOff</p></td>
<td><p>La définition de JET_bitDbShadowingOff désactive la duplication de certaines structures de base de données internes (occultation). La duplication de ces structures étant effectuée à des fins de résilience, la définition de JET_bitDbShadowingOff supprime cette résilience.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errDatabaseDuplicate</p></td>
<td><p>La base de données nommée dans <em>szFilename</em> existe déjà. Lorsque cette erreur est retournée, la base de données n’est pas attachée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Peut être retourné si l’accès exclusif a été demandé, mais n’a pas pu être accordé, ou si une autre session a déjà ouvert la base de données en mode exclusif.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages</p></td>
<td><p>Retourné lorsque <em>cpgDatabaseSizeMax</em> est plus grand que le nombre maximal de pages autorisées dans une base de données. La valeur maximale actuelle est 2147483646 (0x7ffffffe).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>Un chemin d’accès non valide a été spécifié dans <em>szFilename</em>. <em>szFilename</em> doit être non null. Par défaut, <em>szFilename</em> doit pointer vers un répertoire existant. Le chemin d’accès est créé si <em>JET_paramCreatePathIfNotExist</em> est défini (voir <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Indique qu’une autre session a déjà ouvert la base de données en mode exclusif (à l’aide de JET_bitDbExclusive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>La base de données n’a pas été attachée précédemment (voir <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Le fichier de base de données a déjà été attaché par une autre session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Une tentative a été effectuée pour créer une base de données dans une transaction.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Une tentative a été effectuée pour ouvrir un fichier qui n’est pas un fichier de base de données valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>Une tentative a été effectuée pour ouvrir plus d’une base de données et JET_paramOneDatabasePerSession a été définie. Consultez <a href="gg294139(v=exchg.10).md">paramètres système</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Les ressources du système sont insuffisantes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Seul un nombre fini de bases de données peut être attaché par instance. La limite est actuellement de sept bases de données par instance.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>AVERTISSEMENT récupérable indiquant que le fichier de base de données a déjà été attaché par cette session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>JET_wrnFileOpenReadOnly indique que le fichier a été attaché en lecture seule, mais <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> n’a pas réussi JET_bitDbReadOnly. La base de données est toujours ouverte avec un accès en lecture seule.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

Si la base de données spécifiée dans *szFilename* existe et que JET_bitDbOverwriteExisting n’a pas été transmis, l’appel de l’API échoue. Si JET_bitDbOverwriteExisting a été transmis, l’ancien fichier de base de données sera d’abord supprimé.

Si l’API crée un fichier de base de données, puis accède à une autre erreur, il nettoie et supprime le fichier.

**JetCreateDatabase2** ouvre implicitement la base de données. Il n’est pas nécessaire d’appeler ensuite [JetOpenDatabase](./jetopendatabase-function.md).

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
<td><p>Implémenté en tant que <strong>JetCreateDatabase2W</strong> (Unicode) et <strong>JetCreateDatabase2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[Fichiers ESE (Extensible Storage Engine)](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
