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
ms.openlocfilehash: 402326a34a0551262d453b93db2287c69a7160b3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469716"
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


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Identique à JET_errNullInvalid.</p> | 
| <p>JET_errColumnInUse</p> | <p>Cette colonne spécifiée est actuellement utilisée par un index.</p><p><strong>JetSetColumnDefaultValue</strong> ne peut pas modifier la valeur par défaut d’une colonne référencée dans la définition d’un index. Cela est dû au fait que cela peut modifier le contenu de l’index.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonne spécifiée n’existe pas pour cette table.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>L’ID de base de données spécifié n’est pas valide.</p> | 
| <p>JET_errInvalidName</p> | <p>L’un des noms d’objets spécifiés n’est pas valide. Tous les noms d’objets doivent être conformes au même ensemble de règles. Ces règles sont les suivantes :</p><ul><li><p>Les noms d’objets doivent être composés de caractères ASCII.</p></li><li><p>Les noms d’objets doivent comporter au moins un caractère.</p></li><li><p>Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</p></li><li><p>Les noms d’objets ne peuvent pas commencer par un espace.</p></li><li><p>Les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</p></li><li><p>Les noms d’objets ne peuvent pas contenir de point d’exclamation ( !), de point (.), de crochet gauche ([) ou de crochet droit (]).</p></li><li><p>Une fois validée, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet. Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errNullInvalid</p> | <p>La colonne n’a pas pu être définie sur NULL. Cela se produit pour <strong>JetSetColumnDefaultValue</strong> dans les cas suivants :</p><ul><li><p><em>cbData</em> est égal à zéro.</p></li><li><p><strong>pvData</strong> a la valeur null.</p></li></ul><p>Par conséquent, il n’est pas possible de définir la valeur par défaut d’une colonne (arrière) sur NULL ou sur une valeur de longueur nulle.</p> | 
| <p>JET_errObjectNotFound</p> | <p>La table spécifiée n’existe pas pour cette base de données.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTableInUse</p> | <p>Cette table spécifiée est utilisée par une autre session.</p><p><strong>JetSetColumnDefaultValue</strong> requiert un accès exclusif à une table afin de modifier la valeur par défaut de la colonne pour les versions antérieures à Windows Server 2003.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Il n’est pas autorisé de tenter une mise à jour dans l’étendue d’une transaction en lecture seule. Une transaction en lecture seule est une transaction qui a été démarrée à l’aide d’un appel à <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> avec JET_bitTransactionReadOnly. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errWriteConflict</p> | <p>Une autre session a déjà verrouillé l’enregistrement pour la mise à jour. La mise à jour tentée par cette session échoue.</p> | 



En cas de réussite, la valeur par défaut de la colonne spécifiée dans la table donnée dans la base de données donnée est remplacée définitivement par la nouvelle valeur par défaut.

En cas d’échec, aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Il n’est pas possible de modifier la valeur par défaut d’une colonne dans une table de modèle.

Le moteur de base de données tronque en mode silencieux la valeur par défaut d’une colonne à 255 octets pour les colonnes de type long text et long Binary.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetSetColumnDefaultValueW</strong> (Unicode) et <strong>JetSetColumnDefaultValueA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[JetStopService](./jetstopservice-function.md)
