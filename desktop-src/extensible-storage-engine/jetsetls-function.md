---
description: 'En savoir plus sur : fonction JetSetLS'
title: Fonction JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525557"
---
# <a name="jetsetls-function"></a>Fonction JetSetLS


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetsetls-function"></a>Fonction JetSetLS

La fonction **JetSetLS** permet à l’application d’associer un handle de contexte appelé stockage local avec un curseur ou la table associée à ce curseur. Ce descripteur de contexte peut être utilisé par l’application pour stocker les données auxiliaires associées à un curseur ou une table. L’application est notifiée ultérieurement à l’aide d’un rappel d’exécution lorsque le handle de contexte doit être libéré. Cela permet d’associer l’État alloué dynamiquement à un curseur ou une table.

**Windows XP :**  **JetSetLS** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*ls*

Handle de contexte à associer au curseur ou à la table.

Lorsque JET_bitLSReset est spécifié, la valeur réelle de ce paramètre est ignorée et JET_LSNil est utilisé.

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSCursor</p></td>
<td><p>Cette option indique que le handle de contexte doit être associé au curseur donné.</p>
<p>Si ni JET_bitLSCursor ni JET_bitLSTable n’est spécifié, JET_bitLSCursor est présumé.</p>
<p>L’utilisation de cette option avec JET_bitLSTable n’est pas autorisée. L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSReset</p></td>
<td><p>Cette option indique que le handle de contexte spécifié doit être ignoré et que le handle de contexte pour l’objet choisi doit être réinitialisé à JET_LSNil.</p>
<p>Il est important de noter que cette action n’entraîne pas de rappel pour nettoyer la valeur précédente du handle de contexte pour l’objet choisi. Le nettoyage approprié du descripteur de contexte précédent peut être effectué à l’aide de <a href="gg269234(v=exchg.10).md">JetGetLS</a> avec JET_bitLSReset. Pour plus d’informations, consultez <a href="gg269234(v=exchg.10).md">JetGetLS</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Cette option indique que le descripteur de contexte doit être associé à la table associée au curseur donné.</p>
<p>L’utilisation de cette option avec JET_bitLSCursor n’est pas autorisée. L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Code de retour</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>L’opération s’est terminée avec succès.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>L’une des options demandées n’est pas valide, a été utilisée de manière incorrecte ou n’a pas été implémentée. Cela peut se produire pour <strong>JetSetLS</strong> quand JET_bitLSCursor et JET_bitLSTable sont spécifiés.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet</p></td>
<td><p>Le handle de contexte indiqué n’a pas pu être associé à l’objet demandé, car un handle de contexte lui est déjà associé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified</p></td>
<td><p>Le handle de contexte indiqué n’a pas pu être associé à l’objet demandé, car le rappel d’exécution n’a pas été configuré pour l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, le handle de contexte donné a été associé avec succès à l’objet demandé. Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, aucune modification de l’état de l’objet demandé n’est survenue. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Notes

Le stockage local d’un curseur ou d’une table doit être affiché en tant que cache volatile. L’application doit d’abord essayer de récupérer le handle de contexte à l’aide de [JetGetLS](./jetgetls-function.md). Si la valeur n’est pas définie (JET_LSNil), l’application doit créer un nouveau contexte et la charger dans le cache à l’aide de **JetSetLS**. L’application peut purger le cache à l’aide d’un appel à [JetGetLS](./jetgetls-function.md) avec JET_bitLSReset. Si le moteur de base de données vide le cache, un rappel d’exécution sera généré pour permettre à l’application de nettoyer ce contexte. Le type de rappel sera JET_cbtypFreeCursorLS pour un handle de contexte associé à un curseur et JET_cbtypFreeTableLS pour un handle de contexte associé à une table. Dans les deux cas, le handle de contexte est passé en tant que pvArg1. Pour plus d’informations, consultez [JET_CALLBACK](./jet-callback-callback-function.md) .

Le rappel d’exécution doit être configuré correctement pour l’instance associée à la session donnée avant que le stockage local puisse être utilisé. Ce rappel peut être défini à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec [JET_paramRuntimeCallback](./callback-parameters.md). Pour plus d’informations, consultez [JetSetSystemParameter](./jetsetsystemparameter-function.md) et [JET_paramRuntimeCallback](./callback-parameters.md) dans paramètres système.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothèque</strong></p></td>
<td><p>Utilisez ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLS](./jetgetls-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
