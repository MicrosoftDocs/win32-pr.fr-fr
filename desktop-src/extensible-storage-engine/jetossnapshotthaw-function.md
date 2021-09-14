---
description: 'En savoir plus sur : fonction JetOSSnapshotThaw'
title: JetOSSnapshotThaw fonction)
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 445fa1d2370f13ae39615d4228b245899173ad8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126850726"
---
# <a name="jetossnapshotthaw-function"></a>JetOSSnapshotThaw fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetossnapshotthaw-function"></a>JetOSSnapshotThaw fonction)

La fonction **JetOSSnapshotThaw** avertit le moteur qu’il peut reprendre des opérations d’e/s normales après une période de blocage et une capture instantanée réussie.

**Windows xp :****JetOSSnapshotThaw** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*snapId*

Identificateur de la session d’instantané.

*grbit*

Ce paramètre est réservé pour une utilisation ultérieure et la seule valeur valide prise en charge est 0.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>La session d’instantané n’est pas valide ou le paramètre <em>Grbit</em> n’est pas valide.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>La session d’instantané avait un délai d’expiration interne avant l’appel de cet appel. Par conséquent, les opérations d’e/s retournées à normal avant cet appel ont été effectuées.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L’identificateur pour la session d’instantané n’est pas valide.</p> | 



Si cette fonction aboutit, une session d’instantané se termine et le comportement normal du moteur reprend. Une nouvelle session d’instantané peut être démarrée ultérieurement.

Si cette fonction échoue, la session d’instantané en cours se termine, mais le gel d’IOs pendant la période de capture instantanée n’a pas été respecté en interne.

#### <a name="remarks"></a>Notes

Les entrées du journal des événements seront générées pour les différentes étapes de l’instantané.

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
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)
