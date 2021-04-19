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
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520755"
---
# <a name="jetgetls-function"></a>JetGetLS fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgetls-function"></a>JetGetLS fonction)

La fonction **JetGetLS** permet à l’application de récupérer le descripteur de contexte appelé stockage local qui est associé à un curseur ou la table associée à ce curseur. Ce descripteur de contexte doit avoir été défini précédemment à l’aide de [JetSetLS](./jetsetls-function.md). **JetGetLS** peut également être utilisé pour extraire simultanément le descripteur de contexte actuel d’un curseur ou d’une table et réinitialiser ce handle de contexte.

**Windows XP : JetGetLS** est introduit dans Windows XP.

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
<td><p>Indique que le handle de contexte associé au curseur donné doit être récupéré.</p>
<p>Si ni JET_bitLSCursor ni JET_bitLSTable n’est spécifié, JET_bitLSCursor est présumé.</p>
<p>Cette option ne peut pas être utilisée avec JET_bitLSTable. L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSTable</p></td>
<td><p>Indique que le handle de contexte associé à la table qui contient le curseur donné doit être récupéré. L’utilisation de cette option avec JET_bitLSCursor n’est pas autorisée. L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Indique que le handle de contexte pour l’objet choisi doit être réinitialisé à JET_LSNil. La valeur actuelle du handle de contexte est retournée dans la mémoire tampon de sortie.</p></td>
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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p>Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>L’une des options demandées n’est pas valide, utilisée de manière non conforme ou non implémentée.</p>
<p>Cela peut se produire pour <strong>JetGetLS</strong> quand les JET_bitLSCursor et les JET_bitLSTable sont définis.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSNotSet</p></td>
<td><p>Impossible de retourner le descripteur de contexte, car aucun descripteur de contexte n’est actuellement associé à l’objet demandé.</p>
<p><strong>Remarque  </strong> Cette erreur n’est pas renvoyée si JET_bitLSReset est spécifié mais qu’aucun handle de contexte n’a été associé à l’objet demandé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, le handle de contexte a été récupéré à partir de l’objet demandé. Si JET_bitLSReset a été spécifié, ce handle de contexte a également été correctement supprimé de l’objet. Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, aucune modification de l’état de l’objet demandé n’est survenue. Aucune modification de l’état de la base de données ne se produit.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetLS](./jetsetls-function.md)
