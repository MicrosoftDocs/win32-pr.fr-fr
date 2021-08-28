---
description: 'En savoir plus sur : fonction JetDeleteTable'
title: JetDeleteTable fonction)
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cdac49d766835a0d26a3b9d474b8759a552ed1d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984902"
---
# <a name="jetdeletetable-function"></a>JetDeleteTable fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetdeletetable-function"></a>JetDeleteTable fonction)

La fonction **JetDeleteTable** supprime une table dans une base de données ESE.

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*dbid*

Identificateur de base de données à utiliser pour l’appel d’API.

*szTableName*

Nom de la table à supprimer.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errTableInUse</p> | <p>Une tentative a été effectuée pour supprimer une table alors qu’une autre session a un ID de table ouvert (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) avec <a href="gg294118(v=exchg.10).md">JetOpenTable</a> ou <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</p> | 
| <p>Table JET_errCannotDeletetemporary</p> | <p>Une tentative de suppression d’une table temporaire a été effectuée. Une table temporaire est automatiquement supprimée lorsqu’elle est fermée avec <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</p> | 
| <p>JET_errCannotDeleteTemplateTable</p> | <p>Une tentative de suppression d’une table de modèle a été effectuée, autrement dit, une table à partir de laquelle la DDL peut être héritée.</p> | 



#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetDeleteTableW</strong> (Unicode) et <strong>JetDeleteTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JetCloseTable](./jetclosetable-function.md)
