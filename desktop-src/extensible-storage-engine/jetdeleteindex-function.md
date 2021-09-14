---
description: 'En savoir plus sur : fonction JetDeleteIndex'
title: JetDeleteIndex fonction)
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a934581754477f336415926716a9a8c7e6097d81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854163"
---
# <a name="jetdeleteindex-function"></a>JetDeleteIndex fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetdeleteindex-function"></a>JetDeleteIndex fonction)

La fonction **JetDeleteIndex** supprime un index d’une table.

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table qui contient la colonne à supprimer.

*szIndexName*

Nom de l’index à supprimer.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errFixedDDL</p> | <p>Une tentative a été effectuée pour supprimer un index d’une table fixe (par exemple, un index créé avec JET_bitTableCreateFixedDDL).</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>Une tentative de suppression d’un index d’une table de modèle a été effectuée. Une table de modèle a un DDL fixe.</p> | 
| <p>JET_errIndexNotFound</p> | <p>L’index nommé dans <em>szIndexName</em> est introuvable.</p> | 
| <p>JET_errPermissionDenied</p> | <p>La table ne peut pas être mise à jour parce qu’elle a été ouverte en lecture seule.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Plusieurs threads ont tenté d’utiliser la même session de base de données.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transaction a été ouverte en tant que transaction en lecture seule.</p> | 



#### <a name="remarks"></a>Notes

En cas de réussite, l’index est supprimé et ne peut donc pas être utilisé par la suite. Il ne doit y avoir aucune transaction active utilisant l’index.

En cas de réussite, la devise est définie avant le premier enregistrement.

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetDeleteIndexW</strong> (Unicode) et <strong>JetDeleteIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)
