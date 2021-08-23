---
description: 'En savoir plus sur : fonction JetGetLock'
title: JetGetLock fonction)
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfb055c0a11d701e3eabbc4049d85e4e4b77468d97e14fd4506bf04600182f0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979039"
---
# <a name="jetgetlock-function"></a>JetGetLock fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetlock-function"></a>JetGetLock fonction)

La fonction **JetGetLock** fournit un moyen de réserver explicitement la possibilité de mettre à jour une ligne, un verrou en écriture ou d’empêcher explicitement une ligne d’être mise à jour par une autre session, verrou de lecture. Normalement, les verrous d’écriture de ligne sont acquis implicitement en raison de la mise à jour des lignes. Les verrous de lecture ne sont généralement pas requis en raison du contrôle de version des enregistrements. Toutefois, dans certains cas, une transaction peut souhaiter verrouiller explicitement une ligne pour appliquer la sérialisation, ou pour s’assurer qu’une opération suivante réussira en vertu du fait que les verrous requis ont déjà été pris.

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Session qui sera utilisée pour cet appel.

*TableID*

Curseur qui sera utilisé pour cet appel.

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :

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
<td><p>JET_bitReadLock</p></td>
<td><p>Cet indicateur provoque l’acquisition d’un verrou de lecture sur l’enregistrement en cours. Les verrous de lecture sont incompatibles avec les verrous d’écriture déjà détenues par d’autres sessions, mais sont compatibles avec les verrous de lecture détenus par d’autres sessions.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWriteLock</p></td>
<td><p>Cet indicateur provoque l’acquisition d’un verrou d’écriture sur l’enregistrement en cours. Les verrous d’écriture ne sont pas compatibles avec les verrous d’écriture ou de lecture détenus par d’autres sessions, mais sont compatibles avec les verrous de lecture détenus par la même session.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Le <em>Grbit</em> donné n’est ni JET_bitReadLock ni JET_bitWriteLock. Il doit s’agir de l’un de ces deux indicateurs.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Le curseur doit se trouver sur un enregistrement pour pouvoir acquérir un verrou. Les verrous sont des enregistrements Always on.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Les verrous ne peuvent être obtenus que par les sessions dans une transaction.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Le curseur ne peut pas être en lecture seule et acquérir un verrou en écriture.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La session doit avoir des autorisations d’écriture pour acquérir un verrou d’écriture.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>L’erreur retournée lorsqu’un verrou en conflit est demandé.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, la session a acquis le verrou demandé.

En cas d’échec, la session n’a pas acquis le verrou demandé.

#### <a name="remarks"></a>Remarques

Les verrous d’écriture ne peuvent pas être obtenus avec les sessions ou les curseurs qui ont des autorisations en lecture seule, même si la session et le curseur n’effectuent pas d’opération de mise à jour. La session et le curseur doivent tous deux avoir des privilèges d’écriture pour acquérir un verrou d’écriture.

Les verrous de lecture et d’écriture sont un moyen de verrouillage pessimiste. Le verrouillage pessimiste s’attend à ce que plusieurs sessions simultanées soient en conflit et acquièrent des verrous à l’avance pour s’assurer que leurs opérations se déroulent correctement.

La plupart des opérations seront sérialisables en raison des verrous pris implicitement. Toutefois, certaines opérations ne le seront pas. Pour illustrer cela, examinez les deux transactions,

T1 : R (A), U (B)

T2 : R (B), U (A)

Le contrôle de version de l’enregistrement garantit que chaque transaction exécutée simultanément verra les valeurs d’origine pour A et B. Il n’y a pas d’ordre d’exécution en série qui peut produire les mêmes résultats pour A et B dans le cas où les résultats sont dépendants des données lues. Pour que l’application puisse sérialiser cette transaction, elle doit acquérir un verrou de lecture explicite sur A et B dans chaque transaction lorsque la valeur est lue.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p></td>
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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
