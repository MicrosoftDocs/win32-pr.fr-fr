---
description: 'En savoir plus sur : fonction JetDetachDatabase'
title: Fonction JetDetachDatabase
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 028e156cffd5eef0d4baa1f043dddf5105fd1023
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985872"
---
# <a name="jetdetachdatabase-function"></a>Fonction JetDetachDatabase


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetdetachdatabase-function"></a>Fonction JetDetachDatabase

La fonction **JetDetachDatabase** libère un fichier de base de données qui était précédemment attaché à une session de base de données.

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*szFilename*

Nom de la base de données à détacher. Si *szFilename* a la **valeur null** ou est une chaîne vide, toutes les bases de données attachées à *sesid* seront détachées.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBackupInProgress</p> | <p>La base de données est en cours de sauvegarde et ne peut pas être détachée.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>La base de données a été ouverte par <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>. Les bases de données doivent être fermées avant le détachement.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>La base de données n’a pas été attachée précédemment (consultez <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> ou <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p> | 
| <p>JET_errInTransaction</p> | <p>Une tentative de détachement d’une base de données a été effectuée dans une transaction.</p> | 



#### <a name="remarks"></a>Remarques

Si une base de données attachée a été ouverte (avec [JetAttachDatabase](./jetattachdatabase-function.md)), elle doit être fermée avec [JetCloseDatabase](./jetclosedatabase-function.md) avant le détachement.

Windows 2000 uniquement : les bases de données qui n’ont pas été détachées avant l’appel de [JetTerm](./jetterm-function.md) sont automatiquement rattachées lorsque [JetInit](./jetinit-function.md) est appelé par la suite.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetDetachDatabaseW</strong> (Unicode) et <strong>JetDetachDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetTerm](./jetterm-function.md)
