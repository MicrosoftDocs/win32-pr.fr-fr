---
description: 'En savoir plus sur : fonction JetFreeBuffer'
title: JetFreeBuffer fonction)
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7d7b56c38bde931cfe0c1a2e95579a515cf3538
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476435"
---
# <a name="jetfreebuffer-function"></a>JetFreeBuffer fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetfreebuffer-function"></a>JetFreeBuffer fonction)

La fonction **JetFreeBuffer** libère de la mémoire qui a été allouée par un appel du moteur de base de données.

**Windows xp : JetFreeBuffer** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a>Paramètres

*pbBuf*

Pointeur vers une zone de mémoire précédemment allouée par un appel au moteur de base de données. **Null** est acceptable et sera ignoré.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 



#### <a name="remarks"></a>Remarques

Il s’agit d’un comportement indéfini pour passer de la mémoire qui n’a pas été allouée par le moteur de base de données dans à *pbBuf*.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)
