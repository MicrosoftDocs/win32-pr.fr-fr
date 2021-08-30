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
ms.openlocfilehash: e4cbc3f8def16edf7e252865c4b1abcb71db12fe
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981952"
---
# <a name="jetcreatedatabase2-function"></a>Fonction JetCreateDatabase2


_**S’applique à :** Windows | Windows Serveurs_

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


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitDbOverwriteExisting</p> | <p>Par défaut, si <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> ou <strong>JetCreateDatabase2</strong> est appelé et que la base de données existe déjà, l’appel d’API échoue et la base de données d’origine n’est pas remplacée. JET_bitDbOverwriteExisting modifie ce comportement et l’ancienne base de données sera remplacée par une nouvelle. Windows XP et versions ultérieures.</p> | 
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
| <p>JET_errOneDatabasePerSession</p> | <p>Une tentative a été effectuée pour ouvrir plus d’une base de données et JET_paramOneDatabasePerSession a été définie. Consultez <a href="gg294139(v=exchg.10).md">paramètres système</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Les ressources du système sont insuffisantes.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Seul un nombre fini de bases de données peut être attaché par instance. La limite est actuellement de sept bases de données par instance.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>AVERTISSEMENT récupérable indiquant que le fichier de base de données a déjà été attaché par cette session.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>JET_wrnFileOpenReadOnly indique que le fichier a été attaché en lecture seule, mais <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> n’a pas réussi JET_bitDbReadOnly. La base de données est toujours ouverte avec un accès en lecture seule.</p> | 



#### <a name="remarks"></a>Remarques

Si la base de données spécifiée dans *szFilename* existe et que JET_bitDbOverwriteExisting n’a pas été transmis, l’appel de l’API échoue. Si JET_bitDbOverwriteExisting a été transmis, l’ancien fichier de base de données sera d’abord supprimé.

Si l’API crée un fichier de base de données, puis accède à une autre erreur, il nettoie et supprime le fichier.

**JetCreateDatabase2** ouvre implicitement la base de données. Il n’est pas nécessaire d’appeler ensuite [JetOpenDatabase](./jetopendatabase-function.md).

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetCreateDatabase2W</strong> (Unicode) et <strong>JetCreateDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)  
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
