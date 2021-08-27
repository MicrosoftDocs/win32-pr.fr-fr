---
description: 'En savoir plus sur : fonction JetGotoBookmark'
title: JetGotoBookmark fonction)
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54a6370badcdd83e1beed4cc50f42a52eab797ba
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984642"
---
# <a name="jetgotobookmark-function"></a>JetGotoBookmark fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgotobookmark-function"></a>JetGotoBookmark fonction)

La fonction **JetGotoBookmark** positionne un curseur sur une entrée d’index pour l’enregistrement associé au signet spécifié. Le signet peut être utilisé avec n’importe quel index défini sur une table. Le signet d’un enregistrement peut être récupéré à l’aide de [JetGetBookmark](./jetgetbookmark-function.md).

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pvBookmark*

Mémoire tampon qui contient le signet à utiliser pour positionner le curseur.

*cbBookmark*

Taille du signet dans la mémoire tampon.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong>   cette valeur de retour a été introduite dans Windows XP.</p> | 
| <p>JET_errInvalidBookmark</p> | <p>Le signet fourni n’est pas valide. Cela peut être dû au fait que la taille du signet est égale à zéro ou que le pointeur de la mémoire tampon du signet a la <strong>valeur null</strong>.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Le curseur se trouve sur un index secondaire et aucune entrée d’index n’a été trouvée pour l’enregistrement associé au signet.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRecordDeleted</p> | <p>L’enregistrement associé au signet est introuvable.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p><strong>Windows XP :</strong>   cette valeur de retour a été introduite dans Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance associée à la session est en cours d’arrêt.</p> | 



Si cette fonction est réussie, le curseur est positionné sur une entrée d’index pour l’enregistrement associé au signet spécifié. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur, cette plage d’index sera annulée. Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée. Aucune modification de l’état de la base de données ne se produit.

Si cette fonction échoue, la position du curseur reste inchangée. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur, cette plage d’index sera annulée. Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Il existe deux façons d’utiliser un signet pour positionner un curseur sur un index. La première consiste à utiliser le signet pour positionner directement sur l’enregistrement. Cela se produit lorsque l’index actuel du curseur est l’index primaire. Cette technique fonctionne, car un signet ESENT est le même que la clé primaire de l’enregistrement associé.

La deuxième façon d’utiliser un signet est de le positionner sur une entrée dans un index secondaire qui correspond à l’enregistrement associé à ce signet. Pendant ce processus, le moteur recherche l’enregistrement réel à l’aide du signet sur l’index primaire. Il utilise ensuite les données d’enregistrement et la définition d’index secondaire pour calculer une clé dans l’index secondaire qui pointe vers l’enregistrement. Il positionne ensuite le curseur sur l’entrée d’index pour cette clé. Si le curseur se trouve actuellement sur un index secondaire sur une ou plusieurs colonnes clés à valeurs multiples, le curseur est positionné sur l’entrée d’index correspondant à la première valeur multiple de chacune de ces colonnes clés.

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
[JetGetBookmark](./jetgetbookmark-function.md)
