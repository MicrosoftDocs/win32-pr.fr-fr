---
description: 'En savoir plus sur : fonction JetDeleteColumn2'
title: JetDeleteColumn2 fonction)
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2e74c507483791f3090b43e436e01ce7b5173e0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984962"
---
# <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2 fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2 fonction)

La fonction **JetDeleteColumn2** supprime une colonne d’une table de base de données ESE et permet de définir une option *Grbit* .

**Windows xp : JetDeleteColumn2** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table qui contient la colonne à supprimer.

*szColumnName*

Nom de la colonne à supprimer.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitDeleteColumnIgnoreTemplateColumns</p> | <p>La définition de JET_bitDeleteColumIgnoreTemplateColumns oblige l’API à tenter uniquement de supprimer des colonnes dans la table dérivée. Si une colonne de ce nom existe dans la table de base, elle sera ignorée.</p> | 



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

L’appel de [JetDeleteColumn](./jetdeletecolumn-function.md) est identique à l’appel de **JetDeleteColumn2** avec *Grbit* défini sur zéro (0).

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetDeleteColumn2W</strong> (Unicode) et <strong>JetDeleteColumn2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)
