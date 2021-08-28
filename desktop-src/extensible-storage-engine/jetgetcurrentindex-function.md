---
description: 'En savoir plus sur : fonction JetGetCurrentIndex'
title: JetGetCurrentIndex fonction)
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f41114c74643d7165bc16363af3d1777828003b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987682"
---
# <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex fonction)

La fonction **JetGetCurrentIndex** détermine le nom de l’index actuel d’un curseur donné. Ce nom est également utilisé pour resélectionner ultérieurement cet index comme index actuel à l’aide de [JetSetCurrentIndex](./jetsetcurrentindex-function.md). Elle peut également être utilisée pour découvrir les propriétés de cet index à l’aide de [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*szIndexName*

Mémoire tampon de sortie qui reçoit le nom de l’index actuel du curseur.

*cchIndexName*

Taille maximale en caractères de la mémoire tampon de sortie.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>L’opération s’est terminée correctement, mais la mémoire tampon de sortie était trop petite pour recevoir l’intégralité du nom de l’index.</p><p>La mémoire tampon de sortie a été remplie avec la plus grande partie du nom de l’index. Si la mémoire tampon de sortie a au moins un caractère de longueur, la chaîne de cette mémoire tampon de sortie se termine par une valeur null.</p><p><strong>Remarque  </strong> Cette erreur n’est pas renvoyée si cchIndexName est égal à zéro. Pour plus d’informations, consultez la section Notes.</p> | 



En cas de réussite, le nom de l’index actuel du curseur donné sera retourné dans la mémoire tampon de sortie. Si JET_wrnBufferTruncated est retourné, la mémoire tampon de sortie contiendra la plus grande partie du nom d’index, comme dans l’espace prévu à cet effet. Si la mémoire tampon de sortie a au moins un caractère de longueur, alors la chaîne retournée dans cette mémoire tampon se termine par une valeur null. Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, l’état de la mémoire tampon de sortie n’est pas défini. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

S’il n’y a pas d’index actuel pour le curseur, une chaîne vide est retournée. Cela peut se produire lorsque le curseur se trouve sur l’index cluster de la table et qu’aucun index primaire n’a été défini. Cet index est appelé index séquentiel de la table et n’a pas de définition. Dans tous les cas, la définition de l’index actuel sur une chaîne vide à l’aide de [JetSetCurrentIndex](./jetsetcurrentindex-function.md) sélectionne l’index cluster, quelle que soit la présence d’une définition d’index primaire.

Il existe un bogue important dans cette fonction qui est présent dans toutes les versions. Si la mémoire tampon de sortie est trop petite pour recevoir l’intégralité du nom de l’index et que la mémoire tampon de sortie a au moins un caractère de longueur, JET_wrnBufferTruncated ne sera pas retourné. JET_errSuccess est retourné à la place. Pour éviter ce problème, la longueur de la mémoire tampon de sortie doit toujours être d’au moins JET_cbNameMost + 1 (65) caractères.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetGetCurrentIndexW</strong> (Unicode) et <strong>JetGetCurrentIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
