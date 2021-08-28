---
description: 'En savoir plus sur : fonction JetPrepareUpdate'
title: JetPrepareUpdate fonction)
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af1f14d3588077ebc293ab35aeb143cc99b8e440
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986672"
---
# <a name="jetprepareupdate-function"></a>JetPrepareUpdate fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetprepareupdate-function"></a>JetPrepareUpdate fonction)

La fonction **JetPrepareUpdate** est la première opération d’exécution d’une mise à jour, dans le cadre de l’insertion d’un nouvel enregistrement ou du remplacement d’un enregistrement existant par de nouvelles valeurs. Les mises à jour sont effectuées en appelant **JetPrepareUpdate**, puis en appelant [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) zéro, une ou plusieurs fois et enfin en appelant [JetUpdate](./jetupdate-function.md) pour terminer l’opération. **JetPrepareUpdate** et [JetUpdate](./jetupdate-function.md) définissent les limites d’une opération de mise à jour et sont importants pour que seul l’état de mise à jour final d’un enregistrement soit entré dans les index. Cela est à la fois plus efficace, mais également requis dans les cas où les données doivent correspondre à un état valide par rapport à l’opération de définition de colonne.

Il existe différentes options pour l’insertion ou le remplacement des enregistrements, et elles sont décrites plus en détail ci-dessous.

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*préparation*

Options qui peuvent être utilisées pour préparer une mise à jour, notamment les suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_prepCancel</p> | <p>Cet indicateur Force <strong>JetPrepareUpdate</strong> à annuler la mise à jour pour ce curseur.</p> | 
| <p>JET_prepInsert</p> | <p>Cet indicateur force le curseur à préparer une insertion d’un nouvel enregistrement. Toutes les données sont initialisées à l’État par défaut de l’enregistrement. Si la table comporte une colonne à incrémentation automatique, une nouvelle valeur est affectée à cet enregistrement, que la mise à jour réussisse ou non, échoue ou est annulée.</p> | 
| <p>JET_prepInsertCopy</p> | <p>Cet indicateur force le curseur à préparer une insertion d’une copie de l’enregistrement existant. Il doit y avoir un enregistrement actif si cette option est utilisée. L’état initial du nouvel enregistrement est copié à partir de l’enregistrement en cours. Les valeurs longues qui sont stockées hors enregistrement sont virtuellement copiées.</p> | 
| <p>JET_prepInsertCopyDeleteOriginal</p> | <p>Cet indicateur force le curseur à préparer une insertion du même enregistrement, ainsi qu’une suppression ou l’enregistrement d’origine. Il est utilisé dans les cas où la clé primaire a été modifiée.</p> | 
| <p>JET_prepReplace</p> | <p>Cet indicateur force le curseur à préparer un remplacement de l’enregistrement en cours. Si la table contient une colonne version, la colonne version est définie sur la valeur suivante dans sa séquence. Si cette mise à jour ne se termine pas, la valeur de la version dans l’enregistrement n’est pas affectée. Un verrou de mise à jour est appliqué à l’enregistrement pour empêcher d’autres sessions de mettre à jour cet enregistrement avant la fin de cette session.</p> | 
| <p>JET_prepReplaceNoLock</p> | <p>Cet indicateur est similaire à JET_prepReplace, mais aucun verrou n’est pris pour empêcher d’autres sessions de mettre à jour cet enregistrement. Au lieu de cela, cette session peut recevoir des JET_errWriteConflict lorsqu’elle appelle <a href="gg269288(v=exchg.10).md">JetUpdate</a> pour terminer la mise à jour.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errAlreadyPrepared</p> | <p><strong>JetPrepareUpdate</strong> a été appelé avec un indicateur valide pour PREP mais pas JET_prepCancel et le curseur était déjà à l’état préparé.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’indicateur PREP donné n’est pas un indicateur valide.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errNotInTransaction</p> | <p><strong>JetPrepareUpdate</strong> a été appelé pour remplacer un enregistrement qui avait des colonnes SLV. Colonnes SLV. Notez que les colonnes SLV sont une fonctionnalité qui n’est pas destinée à une utilisation générale. cette fonctionnalité est utilisée pour prendre en charge l’infrastructure Microsoft Exchange et n’est pas destinée à être utilisée dans votre application.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errRollbackError</p> | <p><strong>JetPrepareUpdate</strong> a été appelé avec JET_prepCancel mais n’a pas pu restaurer toutes les modifications apportées aux colonnes de type JET_coltypLongText et/ou les colonnes de type JET_coltypLongBinary.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Cet indicateur ne peut pas être utilisé avec la même session à partir de plusieurs threads en même temps. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p><strong>JetPrepareUpdate</strong> a été appelé avec JET_prepCancel mais le curseur n’était pas dans l’état préparé.</p> | 



En cas de réussite, le curseur passe à l’état préparé dans le cadre de la mise à jour souhaitée, ou dans le cas de JET_prepCancel, le curseur est rétabli à l’état non préparé et toutes les modifications sont ignorées.

En cas d’échec, l’état du curseur reste inchangé. Si l’échec a été JET_errRollbackError, l’état du curseur passe à l’état non préparé, mais les modifications ne sont pas toutes annulées.

#### <a name="remarks"></a>Remarques

L’insertion d’une copie d’un enregistrement est une optimisation importante lorsque les enregistrements partagent des données de type JET_coltypLongText et/ou JET_coltypLongBinary. Ces données sont stockées hors-enregistrement lorsqu’elles sont volumineuses et il est possible que plusieurs enregistrements partagent la même représentation physique des données. Dans ce cas, les données peuvent être mises à jour à partir de l’un ou l’autre enregistrement, mais cela entraînera une rafale des données, de sorte que chaque enregistrement possède sa propre copie. Il n’est pas possible de modifier les données d’un enregistrement par une modification d’un autre enregistrement. En outre, il n’est pas possible de bloquer la mise à jour d’un enregistrement à l’aide d’une mise à jour d’un autre enregistrement. Il s’agit d’une fonctionnalité centrale de ESE qui porte le nom de verrouillage au niveau des enregistrements.

Les opérations [JetUpdate](./jetupdate-function.md) qui échouent laissent le curseur dans l’état préparé de mise à jour. Cela permet de corriger certaines erreurs, telles qu’une valeur de colonne incorrecte, sans nécessiter la recréation de l’état de mise à jour. Cela signifie que dans tous les cas où un curseur abandonne une mise à jour, il doit explicitement appeler **JetPrepareUpdate** avec JET_prepCancel.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
