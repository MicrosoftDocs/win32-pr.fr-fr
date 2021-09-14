---
description: 'En savoir plus sur : fonction JetOSSnapshotAbort'
title: JetOSSnapshotAbort fonction)
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7767a1c7e9dc9182fe521d2d903b52d3b88dadb3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520100"
---
# <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort fonction)

La fonction **JetOSSnapshotAbort** avertit le moteur qu’il peut reprendre des opérations d’e/s normales après la fin d’une période de blocage avec un instantané ayant échoué.

**Windows server 2003 :****JetOSSnapshotAbort** est introduite dans Windows server 2003.  

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*snapId*

Identificateur de la session d’instantané.

*grbit*

Options pour cet appel. Ce paramètre est réservé pour une utilisation ultérieure et la seule valeur valide prise en charge est 0 (zéro).

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>La session d’instantané n’est pas valide ou le paramètre Grbit n’est pas valide.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L’identificateur de la session d’instantané n’est pas valide.</p> | 



Si cette fonction est exécutée correctement, la session d’instantané se termine et le comportement normal du moteur reprend. Une nouvelle session d’instantané peut être démarrée ultérieurement.

Si cette fonction échoue, la session d’instantané n’est pas abandonnée.

#### <a name="remarks"></a>Notes

Cette fonction doit être appelée à la place de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) pour informer le moteur que l’instantané a été abandonné pour des raisons qui ne sont pas liées au moteur. Ces informations peuvent être utilisées ultérieurement pour aider à émettre des messages du journal des événements concernant la session d’instantané ou pour aider à déterminer d’autres actions appropriées.

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
