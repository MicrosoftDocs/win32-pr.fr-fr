---
description: 'En savoir plus sur : fonction JetGotoSecondaryIndexBookmark'
title: JetGotoSecondaryIndexBookmark fonction)
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84f9b90d617c11e3e304aa375e25a96b446114da
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984581"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark fonction)

La fonction **JetGotoSecondaryIndexBookmark** positionne un curseur sur une entrée d’index associée au signet de l’index secondaire spécifié. Le signet de l’index secondaire doit être utilisé avec le même index sur la même table que celle à partir de laquelle il a été récupéré à l’origine. Le signet d’index secondaire d’une entrée d’index peut être récupéré à l’aide de **JetGotoSecondaryIndexBookmark**.

**Windows xp :****JetGotoSecondaryIndexBookmark** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pvSecondaryKey*

Mémoire tampon qui contient la clé secondaire à utiliser pour positionner le curseur.

*cbSecondaryKey*

Taille de la clé secondaire dans la mémoire tampon.

*pvPrimaryBookmark*

Mémoire tampon qui contient le signet de clé primaire à utiliser pour positionner le curseur.

*cbPrimaryBookmark*

Taille du signet de clé primaire dans la mémoire tampon.

*grbit*

Groupe de bits qui spécifie zéro, une ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitBookmarkPermitVirtualCurrency</p> | <p>Dans le cas où l’entrée d’index ne peut plus être trouvée, le curseur est placé à gauche de l’emplacement où cette entrée d’index a été trouvée précédemment. L’opération échouera toujours avec JET_errRecordDeleted ; Toutefois, il est possible de passer à l’entrée d’index suivante ou précédente relative à l’entrée d’index manquante.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errInvalidBookmark</p> | <p>Le signet de l’index secondaire fourni n’est pas valide. Cette erreur s’est peut-être produite parce que la clé secondaire est égale à zéro ou que le pointeur de la mémoire tampon de la clé secondaire a la <strong>valeur null</strong>. Cette erreur se produit car</p><ul><li><p>L’index secondaire actuel n’a pas de contrainte d’unicité et la taille du signet fourni est égale à zéro.</p></li><li><p>Le pointeur de la mémoire tampon du signet a la <strong>valeur null</strong>.</p></li></ul> | 
| <p>JET_errNoCurrentIndex</p> | <p>Le curseur ne se trouve pas actuellement sur un index secondaire. Il n’est pas utile d’accéder à un signet d’index secondaire lorsque le curseur n’utilise pas actuellement un index secondaire. <a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> doit être utilisé lorsque le curseur ne se trouve pas sur un index secondaire.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRecordDeleted</p> | <p>L’entrée d’index associée au signet d’index secondaire est introuvable.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p> | 



Si cette fonction est exécutée correctement, le curseur est positionné sur une entrée d’index associée au signet d’index secondaire spécifié. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur, cette plage d’index sera annulée. Si une clé de recherche a été construite pour le curseur à utiliser, cette clé de recherche sera supprimée. Aucune modification de l’état de la base de données ne se produit.

Si cette fonction échoue, la position du curseur reste inchangée, sauf si JET_errRecordDeleted est retourné et JET_bitBookmarkPermitVirtualCurrency est spécifié. Dans ce cas, le curseur est positionné à l’emplacement où l’entrée d’index associée au signet de l’index secondaire spécifié aurait été. Le curseur peut être déplacé par rapport à cette position, mais il n’est pas toujours sur une entrée d’index valide.

Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur, cette plage d’index sera annulée. Si une clé de recherche a été construite pour le curseur à utiliser, cette clé de recherche sera supprimée. Dans tous les cas, aucune modification de l’état de la base de données ne se produit.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)
