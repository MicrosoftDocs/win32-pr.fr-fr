---
description: 'En savoir plus sur : fonction JetRetrieveKey'
title: Fonction JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 65925ce2425dcf717b7db94f5b83ca48a68c8f31
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466217"
---
# <a name="jetretrievekey-function"></a>Fonction JetRetrieveKey


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetretrievekey-function"></a>Fonction JetRetrieveKey

La fonction **JetRetrieveKey** récupère la clé de l’entrée d’index à la position actuelle d’un curseur. Ces clés sont construites par des appels à [JetMakeKey](./jetmakekey-function.md). La clé Récupérée peut ensuite être utilisée pour retourner efficacement ce curseur à la même entrée d’index par un appel à [JetSeek](./jetseek-function.md).

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pvData*

Mémoire tampon de sortie qui recevra la clé.

*cbMax*

Taille maximale, en octets, de la mémoire tampon de sortie.

*pcbActual*

Reçoit la taille réelle, en octets, de la clé.

Si ce paramètre a la valeur NULL, la taille réelle de la clé ne sera pas retournée.

Si la mémoire tampon de sortie est trop petite, la taille réelle de la clé sera toujours retournée. Cela signifie que ce nombre sera supérieur à la taille de la mémoire tampon de sortie.

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Lorsqu’il est spécifié, le moteur retourne la clé de recherche pour le curseur. La clé de recherche est créée à l’aide d’un ou de plusieurs appels antérieurs à <a href="gg269329(v=exchg.10).md">JetMakeKey</a> dans le cadre de la recherche de cette clé à l’aide de <a href="gg294103(v=exchg.10).md">JetSeek</a> ou de la définition d’une plage d’index à l’aide de <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Il n’existe pas de clé de recherche pour le curseur. Cela se produit pour <strong>JetRetrieveKey</strong> si JET_bitRetrieveCopy est spécifié et qu’une clé de recherche n’a pas été construite pour ce curseur à l’aide d’un appel antérieur à <a href="gg269329(v=exchg.10).md">JetMakeKey</a>. La clé de recherche sera supprimée par un appel précédent à n’importe quelle API de navigation sur le curseur autre que <a href="gg294117(v=exchg.10).md">JetMove</a>.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Le curseur n’est pas positionné sur un enregistrement. Cela peut se produire pour de nombreuses raisons différentes. Par exemple, cela se produit si le curseur est actuellement positionné après le dernier enregistrement de l’index actuel.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>L’opération s’est terminée correctement, mais la mémoire tampon de sortie était trop petite pour recevoir la clé entière. Le tampon de sortie a été rempli avec autant de clé que possible. La taille réelle de la clé a également été retournée, si nécessaire.</p><p><strong>Remarque</strong>   Cette erreur ne sera pas retournée si JET_bitRetrieveCopy est spécifié. Pour plus d’informations, consultez la section Notes.</p> | 



En cas de réussite, la clé de l’entrée d’index à la position actuelle d’un curseur est retournée dans la mémoire tampon de sortie. Si JET_wrnBufferTruncated est retourné, la mémoire tampon de sortie contiendra la plus grande partie de la clé telle qu’elle sera contenue dans l’espace fourni et la taille réelle de la clé sera exacte. Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, l’état de la mémoire tampon de sortie et la taille réelle de la clé ne sont pas définis. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Les clés doivent généralement être traitées comme des blocs de données opaques. Aucune tentative n’est faite pour exploiter la structure interne de ces données. Toutefois, les propriétés suivantes peuvent être connues en ce qui concerne toutes les clés ESENT :

  - Les clés peuvent être comparées les unes aux autres à l’aide de la fonction [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) pour établir leur ordre relatif dans l’index d’origine sur la table des entrées d’index source.

  - Il est inutile de comparer les clés des entrées d’index de différents index.

  - la longueur d’une clé est toujours inférieure ou égale à JET_cbKeyMost (255) octets avant Windows Vista. sur Windows Vista et les versions ultérieures, les clés peuvent être plus volumineuses. La taille maximale d’une clé est égale à la valeur actuelle de JET_paramKeyMost.

En plus des propriétés ci-dessus des clés ESENT en général, il est important de noter qu’une clé de recherche est différente de la clé d’une entrée d’index. Plus précisément, une clé de recherche peut être plus longue qu’une clé ordinaire. Cette longueur supplémentaire se produit lorsqu’une option générique est utilisée lors de la construction de la clé de recherche. Pour plus d’informations, consultez [JetMakeKey](./jetmakekey-function.md) .

Il existe un bogue important dans cette API qui est présent dans toutes les versions. Si la clé de recherche est demandée à l’aide de JET_bitRetrieveCopy et que la mémoire tampon de sortie est trop petite pour recevoir la clé entière, JET_wrnBufferTruncated ne sera pas retourné. JET_errSuccess est retourné à la place. Il est important de vérifier que la taille réelle de la clé telle qu’elle est retournée à l’aide de *pcbActual* est inférieure ou égale à la taille de la mémoire tampon de sortie. Si la taille réelle est supérieure à la taille de la mémoire tampon de sortie, l’appelant de **JetRetrieveKey** doit réagir comme si JET_wrnBufferTruncated était retourné à la place.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
