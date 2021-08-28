---
description: 'En savoir plus sur : fonction JetDetachDatabase2'
title: Fonction JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4f29253f3b320abb662f7a4334a14c1c49ed546
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984882"
---
# <a name="jetdetachdatabase2-function"></a>Fonction JetDetachDatabase2


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetdetachdatabase2-function"></a>Fonction JetDetachDatabase2

La fonction **JetDetachDatabase2** libère un fichier de base de données qui était précédemment attaché à une session de base de données.

**Windows xp :****JetDetachDatabase2** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*szFilename*

Nom de la base de données à détacher. Si *szFilename* a la **valeur null** ou est une chaîne vide, toutes les bases de données attachées à *sesid* seront détachées.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitForceCloseAndDetach</p> | <p>Force la fermeture et le détachement de la base de données. Si JET_bitForceCloseAndDetach n’est pas pris en charge, JET_errForceDetachNotAllowed sera retourné.</p> | 
| <p>JET_bitForceDetach</p> | <p>Force le détachement de la base de données. Si JET_bitForceDetach n’est pas pris en charge, JET_errForceDetachNotAllowed sera retourné.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBackupInProgress</p> | <p>La base de données est en cours de sauvegarde et ne peut pas être détachée.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>La base de données a été ouverte par <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>. Les bases de données doivent être fermées avant le détachement.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>La base de données n’a pas été attachée précédemment (consultez <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> ou <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p> | 
| <p>JET_errForceDetachNotAllowed</p> | <p>JET_bitForceDetach n’est pas pris en charge.</p> | 
| <p>JET_errInTransaction</p> | <p>Une tentative de détachement d’une base de données a été effectuée dans une transaction.</p> | 



#### <a name="remarks"></a>Remarques

Si une base de données attachée a été ouverte (avec [JetAttachDatabase](./jetattachdatabase-function.md)), elle doit être fermée avec [JetCloseDatabase](./jetclosedatabase-function.md) avant le détachement.

Windows 2000 uniquement : les bases de données qui n’ont pas été détachées avant l’appel de [JetTerm](./jetterm-function.md) sont automatiquement rattachées lorsque [JetInit](./jetinit-function.md) est appelé par la suite.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetDetachDatabase2W</strong> (Unicode) et <strong>JetDetachDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetInit](./jetinit-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetTerm](./jetterm-function.md)
