---
description: 'En savoir plus sur : fonction JetGetBookmark'
title: JetGetBookmark fonction)
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7806770d528d83f18d6f3eb061dc3043e15a0e53
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984842"
---
# <a name="jetgetbookmark-function"></a>JetGetBookmark fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetbookmark-function"></a>JetGetBookmark fonction)

La fonction **JetGetBookmark** récupère le signet de l’enregistrement associé à l’entrée d’index à la position actuelle d’un curseur. Ce signet peut ensuite être utilisé pour repositionner ce curseur dans le même enregistrement à l’aide de [JetGoToBookmark](./jetgotobookmark-function.md).

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pvBookmark*

Mémoire tampon de sortie qui reçoit le signet.

*cbMax*

Taille maximale, en octets, de la mémoire tampon de sortie.

*pcbActual*

Taille réelle, en octets, du signet.

Si ce paramètre a la **valeur null** , la taille réelle du signet n’est pas retournée.

Si la mémoire tampon de sortie est trop petite, la taille réelle du signet sera toujours retournée. Cela signifie que ce nombre sera supérieur à la taille de la mémoire tampon de sortie.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>L’opération s’est terminée correctement, mais la mémoire tampon de sortie était trop petite pour recevoir l’intégralité du signet. La mémoire tampon de sortie a été remplie avec la plus grande partie du signet. La taille réelle du signet a également été retournée, si nécessaire.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong> ces valeurs de retour sont introduites dans Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Le curseur n’est pas positionné sur un enregistrement. Cela peut se produire pour de nombreuses raisons différentes. Par exemple, cela se produit si le curseur est positionné après le dernier enregistrement de l’index actuel.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p><strong>Windows XP :</strong> cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p> | 



Si cette fonction est réussie, le signet de l’enregistrement qui est associé à l’entrée d’index à la position actuelle d’un curseur est retourné dans la mémoire tampon de sortie. Aucune modification de l’état de la base de données ne se produit.

Si cette fonction échoue, l’état de la mémoire tampon de sortie et la taille réelle du signet ne sont pas définis, sauf si JET_errBufferTooSmall a été retourné. Dans le cas où JET_errBufferTooSmall est retourné, la mémoire tampon de sortie contiendra la plus grande partie du signet qui tient dans l’espace fourni et la taille réelle du signet sera exacte. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Les signets doivent généralement être traités comme des blocs de données opaques. Aucune tentative n’est faite pour exploiter la structure interne de ces données. Toutefois, les conditions suivantes sont vraies pour tous les signets ESENT :

  - Un signet identifie de façon unique un enregistrement dans une table donnée.

  - Le signet d’un enregistrement ne changera pas pendant la durée de vie de cet enregistrement.

  - Le signet d’un enregistrement est le même que la clé de cet enregistrement sur l’index primaire sur la table contenant cet enregistrement. Si aucun index primaire n’est défini sur cette table, le moteur de base de données crée son propre signet pour l’enregistrement.

  - Les signets peuvent être comparés les uns aux autres à l’aide de la fonction [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) pour établir leur classement relatif dans l’index primaire sur la table des enregistrements sources. Si aucun index primaire n’est défini sur cette table, il n’est pas judicieux d’utiliser l’ordre relatif des signets de cette table.

  - Il est inutile de comparer les signets des enregistrements de différentes tables entre eux.

  - un signet est toujours inférieur ou égal à JET_cbBookmarkMost (256) octets en longueur, avant Windows Vista.
    
**Windows Vista :** sur Windows Vista et les versions ultérieures, les signets peuvent être plus volumineux que JET_cbBookmarkMost (256) octets. La taille maximale d’un signet est égale à la valeur actuelle de JET_paramKeyMost + 1.

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
[JetGoToBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
