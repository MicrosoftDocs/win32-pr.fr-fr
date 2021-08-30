---
description: 'En savoir plus sur : fonction JetIntersectIndexes'
title: Fonction JetIntersectIndexes
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 34909de0f732a49711d316affae3eb84487420d3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984502"
---
# <a name="jetintersectindexes-function"></a>Fonction JetIntersectIndexes


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetintersectindexes-function"></a>Fonction JetIntersectIndexes

La fonction **JetIntersectIndexes** calcule l’intersection entre plusieurs jeux d’entrées d’index à partir d’index secondaires différents sur la même table. Cette opération est utile pour Rechercher l’ensemble des enregistrements d’une table qui correspondent à plusieurs critères qui peuvent être exprimés à l’aide de plages d’index.

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*rgindexrange*

Pointeur vers un tableau de structures [JET_IndexRange](./jet-indexrange-structure.md) . Chaque structure inclut une [JET_TABLEID](./jet-tableid.md) qui a été configurée pour contenir l’une des plages d’index à croiser. Pour plus d’informations, consultez [JET_IndexRange](./jet-indexrange-structure.md).

*cindexrange*

Nombre de structures de [JET_IndexRange](./jet-indexrange-structure.md) dans le tableau contenues dans le paramètre *rgindexrange* .

*precordlist*

Pointeur vers une structure [JET_RECORDLIST](./jet-recordlist-structure.md) . Cette structure sera remplie avec suffisamment d’informations pour parcourir la table temporaire avec les résultats de **JetIntersectIndexes**.

Mémoire tampon de sortie qui reçoit une structure [JET_RECORDLIST](./jet-recordlist-structure.md) . La structure contient une description du jeu de résultats de l’intersection.

*grbit*

Réservé pour un usage futur.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>L’une des options demandées n’est pas valide, a été utilisée de manière incorrecte ou n’a pas été implémentée.</p><p>Cette erreur est retournée par <strong>JetIntersectIndexes</strong> quand :</p><p>Le <em>Grbit</em> contenu dans la structure <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> pointée par n’importe quel élément dans le tableau <em>rgindexrange</em> n’est pas égal à JET_bitRecordInIndex.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contient une valeur inattendue ou une valeur qui n’est pas cohérente lorsqu’elle est associée à la valeur d’un autre paramètre.</p><p>Cette erreur est retournée par <strong>JetIntersectIndexes</strong> pour les raisons suivantes :</p><ul><li><p>Le paramètre <em>precordlist</em> a la valeur null.</p></li><li><p>Le membre <strong>cbStruct</strong> de la structure <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> spécifiée dans le paramètre <em>precordlist</em> n’est pas égal à la taille de la structure <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> .</p></li><li><p>Le paramètre <em>cindexrange</em> est égal à zéro.</p></li><li><p>Le paramètre <em>cindexrange</em> est supérieur à 64.</p></li><li><p>Le membre <strong>cbStruct</strong> pour tout élément du tableau spécifié par le paramètre <em>rgindexrange</em> n’est pas égal à la taille de la structure <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> .</p></li><li><p>Les éléments du tableau <em>rgindexrange</em> contiennent <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s de tables différentes.</p></li><li><p>Un élément du tableau <em>rgindexrange</em> contient un <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> qui n’est pas positionné sur un index secondaire.</p></li><li><p>Un ou plusieurs des éléments du tableau <em>rgindexrange</em> contiennent <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s placés sur le même index secondaire.</p></li></ul> | 
| <p>JET_errInvalidSesid</p> | <p>Le descripteur de session n’est pas valide ou fait référence à une session fermée.</p><p>Cette erreur n’est pas retournée dans toutes les circonstances. Les handles ne sont validés qu’à titre d’effort optimal.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas été initialisée.</p> | 
| <p>JET_errOutOfCursors</p> | <p>L’opération a échoué, car le moteur n’a pas pu allouer les ressources nécessaires à l’ouverture d’un nouveau curseur. Les ressources de curseur sont configurées en appelant <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <em>JET_paramMaxCursors</em> spécifié dans le paramètre <em>paramid</em> .</p> | 
| <p>JET_errOutOfMemory</p> | <p>L’opération a échoué, car la mémoire peut être allouée pour être terminée.</p><p><strong>JetIntersectIndexes</strong> peut retourner JET_errOutOfMemory si l’espace d’adressage du processus hôte est trop fragmenté. Le gestionnaire de tables temporaire allouera toujours un segment d’espace d’adressage de 1 Mo pour chaque table temporaire créée, quelle que soit la quantité de données à stocker. <strong>JetIntersectIndexes</strong> crée une table temporaire pour chaque <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> spécifiée dans le paramètre <em>rgindexrange</em> , et une table temporaire pour la sortie dans <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Il n’est pas conforme d’utiliser la même session à partir de plusieurs threads en même temps.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>L’opération a échoué, car le moteur n’a pas pu allouer les ressources nécessaires pour mettre en cache les index de la table. Le nombre d’index dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <em>JET_paramMaxOpenTables</em> spécifié dans le paramètre <em>paramid</em> .</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>L’opération a échoué, car le moteur n’a pas pu allouer les ressources nécessaires pour mettre en cache le schéma de la table. Le nombre de tables dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <em>JET_paramMaxOpenTables</em> spécifié dans le paramètre <em>paramid</em> .</p> | 
| <p>JET_errTooManySorts</p> | <p>L’opération a échoué, car le moteur n’a pas pu allouer les ressources requises pour créer une table temporaire. Les ressources de table temporaire sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec JET_paramMaxTemporaryTables spécifié dans le paramètre <em>paramid</em> .</p> | 



En cas de réussite, une nouvelle table temporaire est retournée, qui contient les signets des enregistrements qui correspondent aux critères représentés par chacune des descriptions de la plage d’index d’entrée.

En cas d’échec, la table temporaire contenant les résultats ne sera pas créée. L’état de la base de données temporaire peut être modifié. L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé. La position actuelle du [JET_TABLEID](./jet-tableid.md)fourni à cette fonction peut être modifiée.

#### <a name="remarks"></a>Remarques

**JetIntersectIndexes** peut être utilisé pour filtrer efficacement les enregistrements d’une table selon plusieurs critères si ces critères peuvent être exprimés en termes d’index secondaires sur cette table. Par exemple, considérez que vous disposez d’une table très volumineuse contenant des personnes. La table peut comporter des colonnes pour son ID utilisateur, son prénom, son nom, etc. Supposons que chacune de ces colonnes soit indexée séparément et que l’index primaire de la table soit sur l’ID d’utilisateur. Si vous souhaitez trouver tous les utilisateurs dont le prénom commence par un et dont le nom commence par G, vous devez effectuer les étapes suivantes :

1.  Ouvrez un nouveau curseur sur la table et définissez ce curseur pour utiliser l’index sur la colonne « First Name ». Configurez ensuite une plage d’index pour toutes les personnes dont le « prénom » a démarré avec « A », puis générez un [JET_IndexRange](./jet-indexrange-structure.md) struct contenant ce curseur.

2.  Répétez l’étape 1 avec un nouveau curseur sur l’index « Last Name » pour toutes les personnes dont le « Last Name » a démarré avec « G ».

3.  Transmettez ces critères à **JetIntersectIndexes** pour calculer le résultat dans une table temporaire.

4.  Parcourez la table temporaire et récupérez chacun des enregistrements qui passent les critères par signet.

La table temporaire contenant le jeu de résultats est une table simple avec une colonne qui contient le signet de chaque enregistrement ayant passé tous les critères utilisés pour calculer l’intersection. Le jeu de résultats est trié dans le même ordre que l’index primaire et ne contient pas d’entrées en double. L’application peut énumérer les résultats de l’intersection en énumérant les lignes de la table temporaire, en extrayant le signet pour chaque résultat à l’aide de [JetRetrieveColumn](./jetretrievecolumn-function.md), puis en visitant l’enregistrement dans la base de données en appelant [JetGotoBookmark](./jetgotobookmark-function.md) avec ce signet sur un curseur positionné sur l’index primaire.

La table temporaire retournée par **JetIntersectIndexes** peut uniquement être analysée vers l’avant. Elle doit également être fermée via [JetCloseTable](./jetclosetable-function.md) lorsque l’analyse est terminée. Pour plus d’informations sur les tables temporaires et leur fonctionnement, consultez [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

**JetIntersectIndexes** est généralement un moyen efficace et pratique de filtrer les enregistrements en fonction de plusieurs critères indexés. Toutefois, il existe des conseils importants qui doivent être suivis pour optimiser l’utilité de cette fonctionnalité. Si vous savez que l’un des critères est tellement restrictif que la plage d’index résultante a très peu d’enregistrements, il est probablement préférable de simplement parcourir la plage d’index et de filtrer les enregistrements au niveau de l’application. En outre, si vous savez que vous avez des critères qui sont bien moins restrictifs que d’autres critères de votre intersection, vous pouvez envisager de supprimer ces critères de plus en moins restrictifs de l’intersection. Enfin, si vous savez que l’un des critères n’est pas tout à fait restrictif, de sorte que la plage d’index résultante est presque aussi importante que l’index primaire, il est peu probable que l’intersection avec cette plage d’index soit avantageuse (réduisez la taille de) l’ensemble de résultats. Dans tous les cas, vous devez sélectionner des critères de manière à ce qu’ils prennent le moins d’entrées d’index possible en entrée et génèrent le jeu de signets le plus spécifique sur la sortie pour des performances maximales.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_IndexRange](./jet-indexrange-structure.md)  
[JET_RECORDLIST](./jet-recordlist-structure.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
