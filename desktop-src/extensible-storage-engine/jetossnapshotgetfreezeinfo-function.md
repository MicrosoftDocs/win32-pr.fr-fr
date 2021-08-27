---
description: 'En savoir plus sur : fonction JetOSSnapshotGetFreezeInfo'
title: JetOSSnapshotGetFreezeInfo fonction)
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e737d6fe31dde43eeba7526e740ec096db20abc9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466206"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a>JetOSSnapshotGetFreezeInfo fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetossnapshotgetfreezeinfo-function"></a>JetOSSnapshotGetFreezeInfo fonction)

La fonction **JetOSSnapshotGetFreezeInfo** récupère la liste des instances et des bases de données qui font partie de la session d’instantané à un moment donné.

**Windows vista :****JetOSSnapshotGetFreezeInfo** est introduit dans Windows vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*snapId*

Identificateur de la session d’instantané à démarrer.

*pcInstanceInfo*

Nombre d’instances en cours d’exécution qui font partie de la session d’instantané.

*paInstanceInfo*

Tableau de structures, une pour chaque instance en cours d’exécution, décrivant l’instance et les bases de données qui en font partie.

*grbit*

Options pour cet appel. Ce paramètre est réservé à un usage futur. La seule valeur valide est 0 (zéro).

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errOutOfMemory</p> | <p>La fonction a échoué en raison d’une condition de mémoire insuffisante.</p> | 
| <p>JET_errInvalidParameter</p> | <p><em>pcInstanceInfo</em> ou <em>PaInstanceInfo</em> a la <strong>valeur null</strong>.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L’identificateur de la session d’instantané n’est pas valide.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Une session d’instantané n’est pas en cours.</p> | 



Si cette fonction est réussie, les informations d’instance sont correctement remplies et doivent être libérées ultérieurement en appelant [JetFreeBuffer](./jetfreebuffer-function.md) avec le pointeur vers le tableau d’informations d’instance retourné.

Si cette fonction échoue, aucune modification de l’état du moteur ne se produit.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) et <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
