---
description: 'En savoir plus sur : fonction JetIndexRecordCount'
title: JetIndexRecordCount fonction)
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ce2f5e6072e1c59820121ca652de9237b1c226f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988992"
---
# <a name="jetindexrecordcount-function"></a>JetIndexRecordCount fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetindexrecordcount-function"></a>JetIndexRecordCount fonction)

La fonction **JetIndexRecordCount** compte le nombre d’entrées dans l’index actuel à partir de la position actuelle vers l’avant. La position actuelle est incluse dans le nombre. Le nombre peut être supérieur au nombre total d’enregistrements dans la table si l’index actuel est sur une colonne à valeurs multiples et que les instances de la colonne ont des valeurs multiples. Si la table est vide, la valeur 0 est retournée pour le nombre.

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pcrec*

Pointeur vers une valeur long non signée pour recevoir le nombre.

*crecMax*

Nombre maximal d’enregistrements à compter. Une valeur *crecMax* de 0 indique que le nombre est illimité.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Le curseur ne se trouve pas actuellement sur un enregistrement et la table n’est pas vide.</p><p><strong>Windows XP, Windows server 2003, Windows 2000 server et Windows 2000 Professional :</strong>  Si le curseur est positionné sur un index ou une plage d’index vide, <strong>JetIndexRecordCount</strong> retourne par erreur JET_errNoCurrentRecord.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p> | 



Si cette fonction a la valeur, le nombre exact d’entrées d’index, y compris la position actuelle et jusqu’à *crecMax* (si elle n’est pas 0), est retourné dans la valeur long pointée longue non signée par *pcrec*.

Si cette fonction échoue, aucune modification n’est apportée à la mémoire allouée sur *precpos*.

#### <a name="remarks"></a>Remarques

Si la table n’est pas vide, le curseur doit être positionné sur l’enregistrement à partir duquel commencer le décompte. Le nombre inclura cet enregistrement, et le nombre sera reporté jusqu’à la limite donnée dans *crecMax*. Si *crecMax* a la valeur 0, l’opération continue à compter jusqu’à la fin de l’index.

Les plages d’index peuvent être utilisées pour construire des limitations de fin d’index artificielles pour le nombre. De cette manière, les sous-plages d’un index peuvent être comptées exactement. Le curseur doit être positionné sur la première ligne de la plage. La fin de la clé de la plage doit être établie, puis [JetSetIndexRange](./jetsetindexrange-function.md) doit être utilisé pour définir la plage supérieure, soit de manière inclusive, soit exclusivement. Enfin, **JetIndexRecordCount** doit être appelé pour compter exactement la plage.

**JetIndexRecordCount** obéit à la sémantique de transaction et retourne un nombre précis pour cette session particulière dans son état transactionnel actuel.

**JetIndexRecordCount** accède aux pages de feuille d’index afin de compter exactement les entrées. Par conséquent, il peut effectuer une grande quantité d’e/s et peut être lent. La limitation *crecMax* doit être utilisée pour empêcher une charge excessive. Si une plage est volumineuse, il peut être possible de compter la plage de manière approximative à l’aide de [JetGetRecordPosition](./jetgetrecordposition-function.md).

**Windows XP, Windows server 2003, Windows 2000 server et Windows 2000 Professional :**  Si le curseur est positionné sur un index ou une plage d’index vide, **JetIndexRecordCount** retourne à tort JET_errNoCurrentRecord plutôt que de retourner un nombre d’enregistrements égal à zéro. Dans ce cas, l’application doit vérifier si l’index ou la plage d’index est vide.

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
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
