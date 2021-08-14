---
description: 'En savoir plus sur : fonction JetSetColumnDefaultValue'
title: JetSetColumnDefaultValue fonction)
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff0f704c30737d6cfc2d8bd823da8207e8d7d8c3fb4458687baf8bc400718304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117703847"
---
# <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue fonction)

La fonction **JetSetColumnDefaultValue** peut être utilisée pour modifier la valeur par défaut d’une colonne existante.

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*dbid*

Base de données à utiliser pour cet appel.

*szTableName*

Nom de la table contenant la colonne qui sera affectée.

*szColumnName*

Nom de la colonne dont la valeur par défaut sera modifiée.

*pvData*

Mémoire tampon d’entrée contenant la nouvelle valeur par défaut.

*cbData*

Taille de la mémoire tampon d’entrée contenant la nouvelle valeur par défaut.

*grbit*

Réservé pour un usage futur.

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
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Identique à JET_errNullInvalid.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnInUse</p></td>
<td><p>Cette colonne spécifiée est actuellement utilisée par un index.</p>
<p><strong>JetSetColumnDefaultValue</strong> ne peut pas modifier la valeur par défaut d’une colonne référencée dans la définition d’un index. Cela est dû au fait que cela peut modifier le contenu de l’index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonne spécifiée n’existe pas pour cette table.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>L’ID de base de données spécifié n’est pas valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>L’un des noms d’objets spécifiés n’est pas valide. Tous les noms d’objets doivent être conformes au même ensemble de règles. Ces règles sont les suivantes :</p>
<ul>
<li><p>Les noms d’objets doivent être composés de caractères ASCII.</p></li>
<li><p>Les noms d’objets doivent comporter au moins un caractère.</p></li>
<li><p>Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</p></li>
<li><p>Les noms d’objets ne peuvent pas commencer par un espace.</p></li>
<li><p>Les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</p></li>
<li><p>Les noms d’objets ne peuvent pas contenir de point d’exclamation ( !), de point (.), de crochet gauche ([) ou de crochet droit (]).</p></li>
<li><p>Une fois validée, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet. Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullInvalid</p></td>
<td><p>La colonne n’a pas pu être définie sur NULL. Cela se produit pour <strong>JetSetColumnDefaultValue</strong> dans les cas suivants :</p>
<ul>
<li><p><em>cbData</em> est égal à zéro.</p></li>
<li><p><strong>pvData</strong> a la valeur null.</p></li>
</ul>
<p>Par conséquent, il n’est pas possible de définir la valeur par défaut d’une colonne (arrière) sur NULL ou sur une valeur de longueur nulle.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>La table spécifiée n’existe pas pour cette base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Cette table spécifiée est utilisée par une autre session.</p>
<p><strong>JetSetColumnDefaultValue</strong> requiert un accès exclusif à une table afin de modifier la valeur par défaut de la colonne pour les versions antérieures à Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Il n’est pas autorisé de tenter une mise à jour dans l’étendue d’une transaction en lecture seule. Une transaction en lecture seule est une transaction qui a été démarrée à l’aide d’un appel à <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> avec JET_bitTransactionReadOnly. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Une autre session a déjà verrouillé l’enregistrement pour la mise à jour. La mise à jour tentée par cette session échoue.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, la valeur par défaut de la colonne spécifiée dans la table donnée dans la base de données donnée est remplacée définitivement par la nouvelle valeur par défaut.

En cas d’échec, aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Il n’est pas possible de modifier la valeur par défaut d’une colonne dans une table de modèle.

Le moteur de base de données tronque en mode silencieux la valeur par défaut d’une colonne à 255 octets pour les colonnes de type long text et long Binary.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetSetColumnDefaultValueW</strong> (Unicode) et <strong>JetSetColumnDefaultValueA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[JetStopService](./jetstopservice-function.md)
