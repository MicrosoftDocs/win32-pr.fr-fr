---
description: 'En savoir plus sur : fonction JetDeleteColumn'
title: JetDeleteColumn fonction)
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c7c73c5a6fd3249a8779526f6655992ad545372
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985912"
---
# <a name="jetdeletecolumn-function"></a>JetDeleteColumn fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetdeletecolumn-function"></a>JetDeleteColumn fonction)

La fonction **JetDeleteColumn** supprime une colonne d’une table de base de données ESE.

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table à partir de laquelle la colonne doit être supprimée.

*szColumnName*

Nom de la colonne à supprimer.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errColumnInUse</p> | <p>La colonne est en cours d’utilisation. Il est peut-être actuellement utilisé par un index.</p> | 
| <p>JET_errFixedDDL</p> | <p>Une tentative de modification du DDL fixe a été effectuée.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>La colonne nommée dans <em>szColumnName</em> existe dans la table de modèle, et la DDL d’une table de modèle ne peut pas être modifiée.</p> | 
| <p>JET_errInvalidName</p> | <p>Cela peut être retourné si un nom incorrect pour <em>szColumnName</em> a été donné.</p> | 
| <p>JET_errPermissionDenied</p> | <p>La table n’est pas accessible en écriture. Cela peut être retourné si la base de données a été ouverte en mode lecture seule.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transaction est une transaction en lecture seule.</p> | 



#### <a name="remarks"></a>Remarques

L’appel de **JetDeleteColumn** est identique à l’appel de [JetDeleteColumn2](./jetdeletecolumn2-function.md) avec *Grbit* défini sur zéro (0).

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetDeleteColumnW</strong> (Unicode) et <strong>JetDeleteColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
