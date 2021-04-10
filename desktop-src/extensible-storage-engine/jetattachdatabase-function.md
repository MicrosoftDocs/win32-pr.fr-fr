---
description: 'En savoir plus sur : fonction JetAttachDatabase'
title: Fonction JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201223"
---
# <a name="jetattachdatabase-function"></a>Fonction JetAttachDatabase


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetattachdatabase-function"></a>Fonction JetAttachDatabase

La fonction **JetAttachDatabase** attache un fichier de base de données à utiliser avec une instance de base de données. Pour pouvoir utiliser la base de données, elle doit être ouverte par la suite avec [JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*szFilename*

Nom de la base de données à attacher.

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
<td><p>JET_bitDbDeleteCorruptIndexes</p></td>
<td><p>Si <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> a été défini, tous les index sur les données Unicode seront supprimés. Pour plus d’informations, consultez la section Notes.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbDeleteUnicodeIndexes</p></td>
<td><p>Tous les index des données Unicode seront supprimés, quel que soit le paramètre de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Pour plus d’informations, consultez la section Notes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbUpgrade</p></td>
<td><p>Obsolète. Ne pas utiliser.</p></td>
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
<td><p>JET_errBackupInProgress</p></td>
<td><p>L’attachement d’une base de données n’est pas autorisé pendant une sauvegarde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>Le fichier de base de données spécifié par <em>szFilename</em> doit être accessible en écriture. L’attribut Read-Only ne doit pas être défini, et le processus en cours d’exécution doit disposer des privilèges suffisants pour écrire dans le fichier.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Le fichier de base de données est déjà ouvert par un autre processus.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>Un chemin d’accès non valide a été spécifié dans <em>szFilename</em>. <em>szFilename</em> doit être non null et faire référence à un chemin d’accès valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Le fichier de base de données a déjà été attaché par une autre session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>Le moteur de base de données ne peut pas ouvrir le fichier de base de données. Le fichier est peut-être utilisé par un autre processus ou l’appelant peut ne pas disposer des privilèges suffisants pour ouvrir le fichier.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileNotFound</p></td>
<td><p>Le fichier spécifié dans <em>szFilename</em> n’existe pas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Il y a une erreur avec l’index primaire. Cela peut provenir d’une corruption physique (par exemple, un disque ou une altération de la mémoire). Elle peut également être retournée lors de l’attachement d’une base de données qui a été modifiée pour la dernière fois sur un système d’exploitation plus ancien et l’index primaire sur une colonne avec des données Unicode. Pour plus d’informations sur les index sur les données Unicode, consultez les notes.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Il y a une erreur avec un index secondaire. Cela peut provenir d’une corruption physique (par exemple, un disque ou une altération de la mémoire). Elle peut également être retournée lors de l’attachement d’une base de données qui a été modifiée pour la dernière fois sur un système d’exploitation plus ancien et un index secondaire sur une colonne avec des données Unicode. Pour plus d’informations sur les index sur les données Unicode, consultez les notes. Les index secondaires sont entièrement reconstruits lorsqu’une base de données est défragmentée à l’aide d’un utilitaire hors connexion à l’aide de la commande suivante : <strong>Esentutl-d</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Seul un nombre fini de bases de données peut être attaché par instance. La limite est actuellement de sept bases de données par instance.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>AVERTISSEMENT récupérable indiquant que le fichier de base de données a déjà été attaché par cette session.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

L’appel de **JetAttachDatabase** équivaut à appeler [JetAttachDatabase2](./jetattachdatabase2-function.md) et à passer une valeur de zéro, ce qui signifie qu’il n’y a aucune limite pour le paramètre *cpgDatabaseSizeMax* .

L’attachement d’une base de données accessible en écriture (autrement dit, si JET_bitDbReadOnly n’a pas été spécifié dans le paramètre *Grbit* ) ouvre le fichier exclusivement au niveau du système d’exploitation. Aucun autre processus ne peut ouvrir le fichier. Il est possible pour plusieurs processus d’attacher une base de données unique en les ouvrant en mode lecture seule.

Le fichier de base de données est détaché à l’aide de [JetDetachDatabase](./jetdetachdatabase-function.md) ou [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Paramètres de vérification d’index

Les différentes versions de Windows normalisent le texte Unicode de différentes façons. Cela signifie que les index créés sous une version de Windows peuvent ne pas fonctionner sur d’autres versions.

Avant Windows Server 2003, lorsque la version du système d’exploitation était modifiée (y compris l’installation d’un service pack), chaque index sur les données Unicode était dans un État potentiellement endommagé.

Les index créés dans Windows Server 2003 et versions ultérieures sont signalés par la version de la normalisation Unicode avec laquelle ils ont été générés. Les index plus anciens ne contiennent pas d’informations sur la version. La plupart des modifications de normalisation Unicode consistent en l’ajout de nouveaux caractères, tandis que les points de code précédemment non définis sont maintenant définis et normalisés différemment. Par conséquent, si les données binaires sont stockées dans une colonne Unicode, elles se normalssent différemment à mesure que de nouveaux points de code sont définis.

À partir de Windows Server 2003, le moteur de base de données ESE effectue le suivi des entrées d’index Unicode qui contiennent des points de code non définis. Elles peuvent être utilisées pour corriger un index lorsque l’ensemble de caractères Unicode définis change.

Ces paramètres contrôlent ce qui se produit lorsque le moteur de base de données ESE est attaché à une base de données qui a été utilisée pour la dernière fois sous une version différente du système d’exploitation. La version du système d’exploitation est marquée dans l’en-tête de la base de données.

Si [JET_paramEnableIndexChecking](./database-parameters.md) a la valeur **true** et que la base de données contient des index potentiellement endommagés :

  - **JetAttachDatabase** supprimera les index potentiellement endommagés si *Grbit* contient JET_bitDbDeleteCorruptIndexes

  - **JetAttachDatabase** renvoie une erreur si *Grbit* ne contient pas de JET_bitDbDeleteCorruptIndexes et si des index doivent être supprimés.

Si [JET_paramEnableIndexChecking](./database-parameters.md) a la valeur **false**:

  - **JetAttachDatabase** ignore les index potentiellement endommagés et retourne JET_errSuccess (en supposant qu’il n’y avait pas d’autres erreurs).

Windows Server 2003 et versions ultérieures : si [JET_paramEnableIndexChecking](./database-parameters.md) n’a pas été réinitialisée, la table de correction interne est utilisée pour corriger les entrées d’index. Cela peut ne pas résoudre tous les endommagements d’index, mais est transparent pour l’application.

Si la base de données a été attachée en lecture seule, l’index ne peut pas être fixe ou supprimé. Dans ce cas, l’API retourne une erreur, par exemple JET_errSecondaryIndexCorrupted ou JET_errPrimaryIndexCorrupted.

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
<td><p>Implémenté en tant que <strong>JetAddColumnW</strong> (Unicode) et <strong>JetAddColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[Fichiers ESE (Extensible Storage Engine)](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetDetachDatabase2](./jetdetachdatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
