---
description: 'En savoir plus sur : fonction JetGetLS'
title: JetGetLS fonction)
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9eb6eed0bbec7be0acd377fa3b34d1b91a8b3fed
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982542"
---
# <a name="jetgetls-function"></a>JetGetLS fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetls-function"></a>JetGetLS fonction)

la fonction **JetGetLS** permet à l’application de récupérer le descripteur de contexte appelé Local Stockage associé à un curseur ou à la table associée à ce curseur. Ce descripteur de contexte doit avoir été défini précédemment à l’aide de [JetSetLS](./jetsetls-function.md). **JetGetLS** peut également être utilisé pour extraire simultanément le descripteur de contexte actuel d’un curseur ou d’une table et réinitialiser ce handle de contexte.

**Windows xp : JetGetLS** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pls*

Mémoire tampon de sortie qui reçoit le handle de contexte actuellement associé au curseur ou à la table.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitLSCursor</p> | <p>Indique que le handle de contexte associé au curseur donné doit être récupéré.</p><p>Si ni JET_bitLSCursor ni JET_bitLSTable n’est spécifié, JET_bitLSCursor est présumé.</p><p>Cette option ne peut pas être utilisée avec JET_bitLSTable. L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</p> | 
| <p>JET_bitLSTable</p> | <p>Indique que le handle de contexte associé à la table qui contient le curseur donné doit être récupéré. L’utilisation de cette option avec JET_bitLSCursor n’est pas autorisée. L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</p> | 
| <p>JET_bitLSReset</p> | <p>Indique que le handle de contexte pour l’objet choisi doit être réinitialisé à JET_LSNil. La valeur actuelle du handle de contexte est retournée dans la mémoire tampon de sortie.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>L’une des options demandées n’est pas valide, utilisée de manière non conforme ou non implémentée.</p><p>Cela peut se produire pour <strong>JetGetLS</strong> quand les JET_bitLSCursor et les JET_bitLSTable sont définis.</p> | 
| <p>JET_errLSNotSet</p> | <p>Impossible de retourner le descripteur de contexte, car aucun descripteur de contexte n’est actuellement associé à l’objet demandé.</p><p><strong>Remarque  </strong> Cette erreur n’est pas renvoyée si JET_bitLSReset est spécifié mais qu’aucun handle de contexte n’a été associé à l’objet demandé.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, le handle de contexte a été récupéré à partir de l’objet demandé. Si JET_bitLSReset a été spécifié, ce handle de contexte a également été correctement supprimé de l’objet. Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, aucune modification de l’état de l’objet demandé n’est survenue. Aucune modification de l’état de la base de données ne se produit.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetLS](./jetsetls-function.md)
