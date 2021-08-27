---
description: 'En savoir plus sur : fonction JetSetCurrentIndex2'
title: Fonction JetSetCurrentIndex2
TOCTitle: JetSetCurrentIndex2 Function
ms:assetid: da94465e-bd35-45c2-9ccc-1d2e8c34aa9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294110(v=EXCHG.10)
ms:contentKeyID: 32765725
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex2W
- JetSetCurrentIndex2A
- JetSetCurrentIndex2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 814813e90446161942775e5c1a26611ed834886f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472485"
---
# <a name="jetsetcurrentindex2-function"></a>Fonction JetSetCurrentIndex2


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetsetcurrentindex2-function"></a>Fonction JetSetCurrentIndex2

La fonction **JetSetCurrentIndex2** définit l’index actuel d’un curseur qui définit les enregistrements d’une table qui sont visibles par ce curseur et l’ordre dans lequel ils apparaissent en sélectionnant l’ensemble d’entrées d’index à utiliser pour exposer ces enregistrements.

```cpp
    JET_ERR JET_API JetSetCurrentIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*szIndexName*

Nom de l’index à sélectionner pour le curseur.

Si ce paramètre a la valeur NULL ou est une chaîne vide, l’index cluster est sélectionné. Si un index primaire est défini pour la table, cet index est sélectionné, car il est identique à l’index cluster. Si aucun index primaire n’est défini pour la table, l’index séquentiel est sélectionné. L’index séquentiel n’a pas de définition d’index. Pour plus d’informations, consultez [JetCreateIndex](./jetcreateindex-function.md) .

Si *pIndexID* n’a pas la valeur null, le nom de l’index sera ignoré et l’index sera sélectionné par son ID d’index.

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitMoveFirst</p> | <p>Cette option indique que le curseur doit être positionné sur la première entrée de l’index spécifié. Si l’index cluster est en cours de sélection (index primaire ou index séquentiel) et si l’index actuel est un index secondaire, JET_bitMoveFirst est supposé. Si l’index actuel est sélectionné, cette option est ignorée et aucune modification n’est apportée à la position du curseur.</p> | 
| <p>JET_bitNoMove</p> | <p>Cette option indique que le curseur doit être positionné sur l’entrée d’index du nouvel index qui correspond à l’enregistrement associé à l’entrée d’index à la position actuelle du curseur sur l’ancien index.</p><p>Si la définition du nouvel index contient au moins une colonne clé à valeurs multiples, l’entrée d’index de destination est ambiguë. Dans ce cas, le <em>itagSequence</em> spécifié est utilisé pour sélectionner la valeur à plusieurs valeurs de la colonne clé à valeurs multiples la plus significative qui est utilisée pour positionner le curseur. Il est seulement nécessaire de passer un seul <em>itagSequence</em> même dans le cas de plusieurs colonnes clés à valeurs multiples, car le moteur étend uniquement toutes les valeurs de la colonne clé à valeurs multiples la plus significative. Pour plus d’informations, consultez <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> .</p><p>Si JET_bitMoveFirst est spécifié, cette option est ignorée.</p><p>Si l’index actuel est sélectionné, cette option est ignorée et aucune modification n’est apportée à la position du curseur. Quand ce paramètre n’est pas présent, sa valeur est supposée être JET_bitMoveFirst.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBadItagSequence</p> | <p>Un index secondaire est sélectionné avec l’option JET_bitNoMove et il n’y a aucune valeur pour la première colonne clé à valeurs multiples dans la nouvelle définition pour l’index qui correspond au numéro de séquence spécifié.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidIndexId</p> | <p>Le contenu de l’ID d’index n’était pas valide ou a expiré et doit être actualisé. Cela peut se produire pour <strong>JetSetCurrentIndex2</strong> dans les cas suivants :</p><ul><li><p>pindexid- &gt; cbStruct n’est pas de la taille attendue (Windows Server 2003 et versions ultérieures).</p></li><li><p>Le moteur a été arrêté depuis que l’ID d’index a été extrait.</p></li><li><p>Tous les curseurs faisant référence à la table contenant l’index correspondant à l’ID d’index ont été fermés et le moteur a supprimé la définition de l’index du cache de schéma.</p></li><li><p>L’ID d’index est utilisé avec un curseur ouvert sur une table incorrecte.</p></li><li><p>L’index a été supprimé ou n’est pas encore visible dans la session.</p></li></ul> | 
| <p>JET_errInvalidName</p> | <p>L’un des noms d’objets spécifiés n’est pas valide. Tous les noms d’objets doivent être conformes au même ensemble de règles. Ces règles sont les suivantes :</p><ul><li><p>Les noms d’objets doivent être composés de caractères ASCII.</p></li><li><p>Les noms d’objets doivent comporter au moins un caractère.</p></li><li><p>Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</p></li><li><p>Les noms d’objets ne peuvent pas commencer par un espace.</p></li><li><p>Les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</p></li><li><p>Les noms d’objets ne peuvent pas contenir de point d’exclamation ( !), de point (.), de crochet gauche ([) ou de crochet droit (]).</p></li><li><p>Une fois validée, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet. Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. cela peut se produire pour <strong>JetSetCurrentIndex2</strong> lorsque <em>pindexid</em> n’a pas la valeur NULL et que pindexid- &gt; cbStruct n’est pas de la taille attendue (Windows XP et versions antérieures).</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Un index secondaire est sélectionné avec l’option JET_bitNoMove et il n’existe aucune entrée d’index dans le nouvel index qui correspond à l’enregistrement associé à l’entrée d’index à la position actuelle du curseur sur l’ancien index.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Le moteur a épuisé son pool de ressources utilisé pour ouvrir les curseurs. Le nombre maximal de curseurs pouvant être ouverts à un moment donné est contrôlé à l’aide de <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>. Pour plus d’informations, consultez <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> . Cela peut se produire pour <strong>JetSetCurrentIndex2</strong> lorsqu’un index secondaire a été sélectionné et que le moteur ne peut pas ouvrir un curseur interne pour utiliser cet index.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, l’index actuel du curseur est défini sur l’index demandé. Les entrées d’index peuvent désormais être recherchées à l’aide de [JetSeek](./jetseek-function.md) en fonction de la définition d’index de l’index demandé. Les entrées d’index peuvent également être énumérées à l’aide de [JetMove](./jetmove-function.md) dans l’ordre spécifié par cette définition d’index. La position actuelle du curseur est définie sur la première entrée d’index de l’index (JET_bitMoveFirst) ou sur une entrée d’index spécifique qui est associée à la position actuelle du curseur sur l’ancien index (JET_bitNoMove). Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, l’index actuel et la position actuelle du curseur sont dans un État indéfini. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Si l’indicateur d’ID d’index est obsolète, l’API échoue simplement. Il n’existe pas de secours pour le nom de texte de l’index dans ce cas, car il peut s’agir d’un exemple. Ce secours doit être effectué manuellement par l’appelant de l’API.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetSetCurrentIndex2W</strong> (Unicode) et <strong>JetSetCurrentIndex2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetGetCurrentIndex](./jetgetcurrentindex-function.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetSeek](./jetseek-function.md)  
[JetStopService](./jetstopservice-function.md)
