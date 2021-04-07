---
description: 'En savoir plus sur : fonction JetOpenDatabase'
title: Fonction JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760539"
---
# <a name="jetopendatabase-function"></a>Fonction JetOpenDatabase


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetopendatabase-function"></a>Fonction JetOpenDatabase

La fonction **JetOpenDatabase** ouvre une base de données précédemment attachée, à l’aide des fonctions [JetAttachDatabase](./jetattachdatabase-function.md) ou [JetAttachDatabase2](./jetattachdatabase2-function.md) , pour une utilisation avec une session de base de données. Cette fonction peut être appelée plusieurs fois pour la même base de données.

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*szFilename*

Nom de la base de données à ouvrir.

*szConnect*

Réservé. valeur de l’en-tête définie sur Null.

*pdbid*

Pointeur vers une mémoire tampon qui, sur un appel réussi, contient l’identificateur de la base de données. Si l’appel échoue, la valeur n’est pas définie.

*grbit*

Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.

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
<td><p>JET_bitDbExclusive</p></td>
<td><p>Autorise une seule session à attacher une base de données. En règle générale, plusieurs sessions peuvent ouvrir une base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbReadOnly</p></td>
<td><p>Empêche toute modification de la base de données.</p></td>
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
<td><p>JET_errDatabaseInUse</p></td>
<td><p>L’accès exclusif a été demandé, mais n’a pas pu être accordé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>Un chemin d’accès non valide a été spécifié dans <em>szFilename</em>. <em>szFilename</em> doit être non null et faire référence à un fichier valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Une autre session a déjà ouvert la base de données en mode exclusif (à l’aide de JET_bitDbExclusive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>La base de données n’a pas été attachée précédemment (voir <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Une tentative a été effectuée pour ouvrir un fichier qui n’est pas un fichier de base de données valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>Une tentative a été effectuée pour ouvrir plus d’une base de données et <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> a été définie. Pour plus d’informations, consultez <a href="gg294139(v=exchg.10).md">paramètres système</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>Le fichier a été attaché en lecture seule, mais <strong>JetOpenDatabase</strong> n’a pas réussi JET_bitDbReadOnly. La base de données est toujours ouverte avec un accès en lecture seule.</p></td>
</tr>
</tbody>
</table>


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
<td><p>Implémenté en tant que <strong>JetOpenDatabaseW</strong> (Unicode) et <strong>JetOpenDatabaseA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
