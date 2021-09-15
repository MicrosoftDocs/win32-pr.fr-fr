---
description: 'En savoir plus sur : fonction JetAttachDatabase2'
title: Fonction JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02f896d41c5804fd85a3cb5f31b6c509c3099357
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530005"
---
# <a name="jetattachdatabase2-function"></a>Fonction JetAttachDatabase2


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetattachdatabase2-function"></a>Fonction JetAttachDatabase2

La fonction **JetAttachDatabase2** attache un fichier de base de données pour une utilisation avec une instance de base de données et spécifie une taille maximale pour cette base de données. Pour pouvoir utiliser la base de données, elle doit être ouverte par la suite avec [JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de session de base de données qui sera utilisé pour l’appel d’API.

*szFilename*

Nom de la base de données à attacher.

*cpgDatabaseSizeMax*

Taille maximale, en pages de base de données, pour la base de données. La taille de page de la base de données par défaut est de 4 kilo-octets, qui peut être modifiée à l’aide de la fonction [JetSetSystemParameter](./jetsetsystemparameter-function.md) avant de créer une base de données.

Le fait de passer la valeur zéro signifie qu’il n’y a pas de valeur maximale appliquée par le moteur de base de données.

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Si <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> a été défini, tous les index sur les données Unicode seront supprimés. Pour plus d’informations, consultez la section Notes.</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Tous les index des données Unicode seront supprimés, quel que soit le paramètre de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Pour plus d’informations, consultez la section Notes.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Empêche toute modification de la base de données.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Réservé pour un usage futur.</p> | 



### <a name="return-value"></a>Valeur renvoyée

La fonction retourne l’un des codes d’erreur [JET_ERR](./jet-err.md) . Les éléments suivants sont les plus couramment renvoyés. (pour obtenir la liste complète des erreurs pour cette API, consultez [Codes d’erreur du moteur d’Stockage Extensible](./extensible-storage-engine-error-codes.md).)


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBackupInProgress</p> | <p>L’attachement d’une base de données n’est pas autorisé pendant une sauvegarde.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>Le fichier de base de données spécifié par <em>szFilename</em> doit être accessible en écriture. L’attribut Read-Only ne doit pas être défini, et le processus en cours d’exécution doit disposer des privilèges suffisants pour écrire dans le fichier.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Le fichier de base de données est déjà ouvert par un autre processus.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Un chemin d’accès non valide a été spécifié dans <em>szFilename</em>. <em>szFilename</em> doit être non null et faire référence à un chemin d’accès valide.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Le fichier de base de données a déjà été attaché par une autre session.</p> | 
| <p>JET_errFileNotFound</p> | <p>Le fichier spécifié dans <em>szFilename</em> n’existe pas.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Il y a une erreur avec l’index primaire. Cela peut provenir d’une corruption physique (par exemple, un disque ou une altération de la mémoire). Elle peut également être retournée lors de l’attachement d’une base de données qui a été modifiée pour la dernière fois sur un système d’exploitation plus ancien et l’index primaire sur une colonne avec des données Unicode. Pour plus d’informations sur les index sur les données Unicode, consultez les notes.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Il y a une erreur avec un index secondaire. Cela peut provenir d’une corruption physique (par exemple, un disque ou une altération de la mémoire). Elle peut également être retournée lors de l’attachement d’une base de données qui a été modifiée pour la dernière fois sur un système d’exploitation plus ancien et un index secondaire sur une colonne avec des données Unicode. Pour plus d’informations sur les index sur les données Unicode, consultez les notes. Les index secondaires sont entièrement reconstruits lorsqu’une base de données est défragmentée à l’aide d’un utilitaire hors connexion à l’aide de la commande suivante : <strong>Esentutl-d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Seul un nombre fini de bases de données peut être attaché par instance. La limite est actuellement de sept bases de données par instance.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>AVERTISSEMENT récupérable indiquant que le fichier de base de données a déjà été attaché par cette session.</p> | 



#### <a name="remarks"></a>Notes

Le fichier de base de données est détaché à l’aide de [JetDetachDatabase](./jetdetachdatabase-function.md) ou [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Consultez [JetAttachDatabase](./jetattachdatabase-function.md) pour les remarques.

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetAttachDatabase2W</strong> (Unicode) et <strong>JetAttachDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
