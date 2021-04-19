---
description: 'En savoir plus sur : fonction JetSetTableSequential'
title: JetSetTableSequential fonction)
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536965"
---
# <a name="jetsettablesequential-function"></a>JetSetTableSequential fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetsettablesequential-function"></a>JetSetTableSequential fonction)

La fonction **JetSetTableSequential** avertit le moteur de base de données que l’application analyse l’intégralité de l’index actuel qui contient un curseur donné. Par conséquent, les méthodes utilisées pour accéder aux données d’index seront paramétrées pour rendre ce scénario aussi rapide que possible.

**Windows XP :**  **JetSetTableSequential** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*grbit*

Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.

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
<td><p>JET_bitPrereadForward</p></td>
<td><p>Cette option est utilisée pour indexer vers l’avant.</p>
<p><strong>Windows 7 :</strong>  <strong>JET_bitPrereadForward</strong> est introduite dans Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitPrereadBackward</p></td>
<td><p>Cette option est utilisée pour indexer dans le sens inverse.</p>
<p><strong>Windows 7 :</strong>  <strong>JET_bitPrereadBackward</strong> est introduite dans Windows 7.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été suspendue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


Si cette fonction fonctionne, l’index actuel du curseur est optimisé pour une analyse séquentielle de la totalité de l’index. Aucune modification de l’état de la base de données ne se produit.

Si cette fonction échoue, aucune modification de la configuration du curseur ne se produit. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Notes

Si l’application doit analyser efficacement un sous-ensemble connu d’un index, une optimisation similaire est également effectuée chaque fois qu’une plage d’index est établie à l’aide de [JetSetIndexRange](./jetsetindexrange-function.md). Cette optimisation est disponible uniquement sur Windows XP et les versions ultérieures.

Si l’application doit analyser efficacement un sous-ensemble inconnu d’un index, aucune action ne doit être effectuée. Le moteur peut détecter automatiquement le comportement de l’analyse et récupérer les données à l’avance. Toutefois, ce comportement n’est pas aussi agressif.

Cette optimisation rendra l’analyse efficace de l’index principal et fera en sorte que l’analyse des données d’entrée d’index dans un index secondaire soit efficace. Il n’effectue pas l’analyse d’un index secondaire pendant la récupération des données d’enregistrement. Cela est dû au fait que le moteur n’effectue pas de lecture anticipée sur les données de l’enregistrement.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
