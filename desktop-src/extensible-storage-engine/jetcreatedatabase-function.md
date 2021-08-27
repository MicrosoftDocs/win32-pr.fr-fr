---
description: 'En savoir plus sur : fonction JetCreateDatabase'
title: Fonction JetCreateDatabase
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 572684785139bd8cdcd0da391199bdf6b5cb0bd9
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985072"
---
# <a name="jetcreatedatabase-function"></a>Fonction JetCreateDatabase


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetcreatedatabase-function"></a>Fonction JetCreateDatabase

La fonction **JetCreateDatabase** crée et attache un fichier de base de données à utiliser avec le moteur de base de données ESE. L’appel de [JetCreateDatabase2](./jetcreatedatabase2-function.md) avec *cpgDatabaseSizeMax* défini à zéro est identique à l’appel de **JETCREATEDATABASE** avec *szConnect* défini sur null. Actuellement, jusqu’à sept bases de données peuvent être créées par instance.

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*szFilename*

Nom de la base de données à créer.

*szConnect*

Réservé pour un usage futur. valeur de l’en-tête définie sur Null.

*pdbid*

Pointeur vers une mémoire tampon qui, sur un appel réussi, contient l’identificateur de la base de données. En cas d’échec, la valeur n’est pas définie.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitDbOverwriteExisting</p> | <p>Par défaut, si <strong>JetCreateDatabase</strong> est appelé et que la base de données existe déjà, l’appel d’API échoue et la base de données d’origine n’est pas remplacée. JET_bitDbOverwriteExisting modifie ce comportement et l’ancienne base de données sera remplacée par une nouvelle. Windows XP et versions ultérieures.</p> | 
| <p>JET_bitDbRecoveryOff</p> | <p>JET_bitDbRecoveryOff désactive la journalisation. La définition de ce bit perd la possibilité de relire les fichiers journaux et de récupérer la base de données à un État utilisable cohérent après un événement catastrophique.</p> | 
| <p>JET_bitDbShadowingOff</p> | <p>La définition de JET_bitDbShadowingOff désactive la duplication de certaines structures de base de données internes (occultation). La duplication de ces structures étant effectuée à des fins de résilience, la définition de JET_bitDbShadowingOff supprime cette résilience.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errDatabaseDuplicate</p> | <p>La base de données nommée dans <em>szFilename</em> existe déjà. Lorsque cette erreur est retournée, la base de données n’est pas attachée.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Peut être retourné si l’accès exclusif a été demandé, mais n’a pas pu être accordé, ou si une autre session a déjà ouvert la base de données en mode exclusif.</p> | 
| <p>JET_errDatabaseInvalidPages</p> | <p>Retourné lorsque <em>cpgDatabaseSizeMax</em> est plus grand que le nombre maximal de pages autorisées dans une base de données. La valeur maximale actuelle est 2147483646 (0x7ffffffe).</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Un chemin d’accès non valide a été spécifié dans <em>szFilename</em>. <em>szFilename</em> doit être non null. Par défaut, <em>szFilename</em> doit pointer vers un répertoire existant. Le chemin d’accès est créé si <em>JET_paramCreatePathIfNotExist</em> est défini (voir <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Indique qu’une autre session a déjà ouvert la base de données en mode exclusif (à l’aide de JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>La base de données n’a pas été attachée précédemment (voir <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Le fichier de base de données a déjà été attaché par une autre session.</p> | 
| <p>JET_errInTransaction</p> | <p>Une tentative a été effectuée pour créer une base de données dans une transaction.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Une tentative a été effectuée pour ouvrir un fichier qui n’est pas un fichier de base de données valide.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Une tentative a été effectuée pour ouvrir plus d’une base de données et JET_paramOneDatabasePerSession a été définie. Consultez <a href="gg269337(v=exchg.10).md">paramètres de la base de données</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L’opération a échoué car la mémoire n’a pas pu être allouée.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Seul un nombre fini de bases de données peut être attaché par instance. La limite est actuellement de sept bases de données par instance.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>AVERTISSEMENT récupérable indiquant que le fichier de base de données a déjà été attaché par cette session.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>JET_wrnFileOpenReadOnly indique que le fichier a été attaché en lecture seule, mais <strong>JetCreateDatabase</strong> n’a pas réussi JET_bitDbReadOnly. La base de données est toujours ouverte avec un accès en lecture seule.</p> | 



#### <a name="remarks"></a>Remarques

Si la base de données spécifiée dans *szFilename* existe et que JET_bitDbOverwriteExisting n’a pas été transmis, l’appel de l’API échoue. Si JET_bitDbOverwriteExisting a été transmis, l’ancien fichier de base de données sera d’abord supprimé.

Si l’API crée un fichier de base de données, puis accède à une autre erreur, il nettoie et supprime le fichier.

**JetCreateDatabase** ouvre implicitement la base de données. Il n’est pas nécessaire d’appeler par la suite [JetOpenDatabase](./jetopendatabase-function.md).

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetCreateDatabaseW</strong> (Unicode) et <strong>JetCreateDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
