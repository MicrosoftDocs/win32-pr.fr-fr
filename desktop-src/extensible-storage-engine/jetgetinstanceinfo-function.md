---
description: 'En savoir plus sur : fonction JetGetInstanceInfo'
title: JetGetInstanceInfo fonction)
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4abec75ccb8e444d4689fea65514fea9a6538e8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988572"
---
# <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo fonction)

La fonction **JetGetInstanceInfo** récupère des informations sur les instances qui sont en cours d’exécution.

**Windows xp : JetGetInstanceInfo** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Paramètres

*pcInstanceInfo*

Pointeur vers une mémoire tampon qui reçoit le nombre d’éléments stockés dans *paInstanceInfo*.

*paInstanceInfo*

Pointeur vers une mémoire tampon qui reçoit l’adresse du premier élément d’un tableau de structures.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cette erreur est retournée par <strong>JetGetInstanceInfo</strong> quand :</p><ul><li><p><em>pcInstanceInfo</em> ou <em>paInstanceInfo</em> ont la valeur null.</p></li></ul> | 
| <p>JET_errOutOfMemory</p> | <p>La mémoire est insuffisante pour traiter la demande.</p> | 



#### <a name="remarks"></a>Remarques

Le moteur de base de données alloue un tableau de structures de [JET_INSTANCE_INFO](./jet-instance-info-structure.md) . L’appelant est chargé de libérer cette mémoire avec [JetFreeBuffer](./jetfreebuffer-function.md).

S’il n’y a aucune instance active, **JetGetInstanceInfo** retourne JET_errSuccess et *pcInstanceInfo* reçoit la valeur 0.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetGetInstanceInfoW</strong> (Unicode) et <strong>JetGetInstanceInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)
