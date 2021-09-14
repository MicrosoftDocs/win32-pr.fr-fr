---
description: 'En savoir plus sur : fonction JetGetRecordSize2'
title: JetGetRecordSize2 fonction)
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 62bae938603407897105939138b74bec77acc324
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915888"
---
# <a name="jetgetrecordsize2-function"></a>JetGetRecordSize2 fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetrecordsize2-function"></a>JetGetRecordSize2 fonction)

La fonction **JetGetRecordSize2** récupère les informations sur la taille des enregistrements à partir de l’emplacement souhaité.

**Windows 7 : JetGetRecordSize2** est introduit dans le système d’exploitation Windows 7.

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Identifie le contexte de session de base de données qui sera utilisé pour l’appel d’API.

*TableID*

Identifie la table ou le curseur qui sera utilisé pour l’appel d’API. Le curseur doit être positionné sur un enregistrement ou avoir une mise à jour préparée.

*precsize*

Pointeur vers une mémoire tampon de sortie pour la structure [JET_RECSIZE2](./jet-recsize2-structure.md) .

*grbit*

Il s’agit d’une ou plusieurs des valeurs suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>Cela récupère la taille de l’enregistrement qui se trouve dans le tampon de copie préparé pour la mise à jour. Dans le cas contraire, l' <em>TableID</em> ou le curseur doit être positionné sur un enregistrement et cet enregistrement sera utilisé.</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>Lorsque ce bit est spécifié, le <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> n’est pas mis à zéro avant de remplir le contenu, ce qui agit efficacement comme une accumulation des statistiques pour plusieurs enregistrements visités ou mis à jour.</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>Ainsi, l’API ignore les valeurs longues non intrinsèques. Par exemple, seul l’enregistrement local de la page sera utilisé.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>L’une des options demandées n’est pas valide ou n’est pas implémentée. Cette erreur est retournée par la fonction <strong>JetGetRecordSize2</strong> lorsqu’un <em>Grbit</em> illégal est spécifié.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas été initialisée.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong> JET_errInstanceUnavailable ne sont retournées que par le système d’exploitation Windows XP et les versions ultérieures de Windows.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Il n’est pas conforme d’utiliser la même session pour plusieurs threads en même temps.</p><p><strong>Windows XP :</strong> les JET_errInstanceUnavailable sont retournées uniquement par Windows XP et les versions ultérieures de Windows.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Cela peut se produire si le curseur a été placé de manière incorrecte.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Si le curseur n’est pas positionné dans une transaction, cela peut se produire si un autre thread supprime l’enregistrement de cette session.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Peut être retourné si une precsize <strong>null</strong><em></em> a été passée.</p> | 



#### <a name="remarks"></a>Notes

La taille de la clé accumulée dans le champ **cbOverhead** de [JET_RECSIZE2](./jet-recsize2-structure.md)est affectée par JET_bitRecordSizeInCopyBuffer. Si ce bit est spécifié, la taille de clé accumulée dans le champ **cbOverhead** est la taille de la clé complète. Si ce bit n’est pas utilisé, la taille cumulée de la clé n’inclut pas la taille enregistrée en raison de la compression de préfixe de clé.

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)
