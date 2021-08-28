---
description: 'En savoir plus sur : fonction JetGetSecondaryIndexBookmark'
title: JetGetSecondaryIndexBookmark fonction)
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0773842d7de7d576e9ccbcab2c62ec456912a89
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984822"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark fonction)

La fonction **JetGetSecondaryIndexBookmark** récupère un signet spécial pour l’entrée d’index secondaire à la position actuelle d’un curseur. Ce signet peut ensuite être utilisé pour repositionner efficacement ce curseur sur la même entrée d’index à l’aide de [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md). Cela est particulièrement utile lors du repositionnement sur un index secondaire qui contient des clés dupliquées ou qui contient plusieurs entrées d’index pour le même enregistrement.

**Windows xp : JetGetSecondaryIndexBookmark** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pvSecondaryKey*

Mémoire tampon de sortie qui reçoit la clé secondaire.

*cbSecondaryKeyMax*

Taille maximale, en octets, de la mémoire tampon de sortie pour la clé secondaire.

*pcbSecondaryKeyActual*

Reçoit la taille réelle, en octets, de la clé secondaire.

Si ce paramètre a la valeur NULL, la taille réelle de la clé secondaire n’est pas retournée.

Si la mémoire tampon de sortie est trop petite, la taille réelle de la clé secondaire est toujours retournée. Cela signifie que ce nombre sera supérieur à la taille de la mémoire tampon de sortie.

*pvPrimaryBookmark*

Mémoire tampon de sortie qui reçoit le signet de clé primaire.

*cbPrimaryBookmarkMax*

Taille maximale, en octets, de la mémoire tampon de sortie pour le signet de clé primaire.

*pcbPrimaryKeyActual*

Reçoit la taille réelle, en octets, du signet de clé primaire.

Si ce paramètre a la valeur NULL, la taille réelle du signet de clé primaire n’est pas retournée.

Si la mémoire tampon de sortie est trop petite, la taille réelle du signet de clé primaire sera toujours retournée. Cela signifie que ce nombre sera supérieur à la taille de la mémoire tampon de sortie.

*grbit*

Réservé pour un usage futur.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>L’opération s’est terminée correctement, mais l’une des mémoires tampons de sortie était trop petite pour recevoir les données demandées.</p><p>La mémoire tampon de sortie a été remplie avec la plus grande partie du signet. La taille réelle du signet a également été retournée, si nécessaire.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Le curseur ne se trouve pas actuellement sur un index secondaire.</p><p>Il n’est pas utile de récupérer un signet d’index secondaire lorsque le curseur n’utilise pas actuellement un index secondaire. <a href="gg269221(v=exchg.10).md">JetGetBookmark</a> doit être utilisé lorsque le curseur ne se trouve pas sur un index secondaire.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Le curseur n’est pas positionné sur un enregistrement.</p><p>Cela peut se produire pour de nombreuses raisons différentes. Par exemple, cela se produit si le curseur est actuellement positionné après le dernier enregistrement de l’index actuel.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, le signet d’index secondaire de l’entrée d’index à la position actuelle d’un curseur est retourné dans les tampons de sortie. Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, l’état des tampons de sortie et la taille réelle du signet de l’index secondaire ne sont pas définis, sauf si JET_errBufferTooSmall a été retourné. Dans le cas où JET_errBufferTooSmall est retourné, les tampons de sortie contiendront la plus grande partie du signet d’index secondaire, comme dans l’espace fourni et la taille réelle du signet d’index secondaire sera exacte. Dans tous les cas, aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Les signets doivent généralement être traités comme des blocs de données opaques. Aucune tentative n’est faite pour exploiter la structure interne de ces données. Toutefois, les propriétés suivantes peuvent être connues en ce qui concerne tous les signets ESENT :

  - Un signet identifie de façon unique un enregistrement dans une table donnée.

  - Le signet d’un enregistrement ne changera pas pendant la durée de vie de cet enregistrement.

  - Le signet d’un enregistrement est le même que la clé de cet enregistrement sur l’index primaire sur la table contenant cet enregistrement. Si aucun index primaire n’est défini sur cette table, le moteur de base de données crée son propre signet pour l’enregistrement.

  - Les signets peuvent être comparés les uns aux autres à l’aide de [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) pour établir leur ordre relatif dans l’index primaire sur la table des enregistrements sources. Si aucun index primaire n’est défini sur cette table, l’ordre relatif des signets de cette table n’est pas significatif.

  - Il est inutile de comparer les signets des enregistrements de différentes tables entre eux.

  - un signet est toujours inférieur ou égal à JET_cbBookmarkMost (256) octets de longueur avant Windows Vista. sur Windows Vista et les versions ultérieures, les signets peuvent être plus volumineux. La taille maximale d’un signet est égale à la valeur actuelle de JET_paramKeyMost + 1.

Les clés doivent généralement être traitées comme des blocs de données opaques. Aucune tentative n’est faite pour exploiter la structure interne de ces données. Toutefois, les propriétés suivantes peuvent être connues en ce qui concerne toutes les clés ESENT :

  - Les clés peuvent être comparées les unes aux autres à l’aide de [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) pour établir leur ordre relatif dans l’index d’origine sur la table des entrées d’index source.

  - Il est inutile de comparer les clés des entrées d’index de différents index.

  - la longueur d’une clé est toujours inférieure ou égale à JET_cbKeyMost (255) octets avant Windows Vista. sur Windows Vista et les versions ultérieures, les clés peuvent être plus volumineuses. La taille maximale d’une clé est égale à la valeur actuelle de JET_paramKeyMost.

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
[JetGetBookmark](./jetgetbookmark-function.md)  
[JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
