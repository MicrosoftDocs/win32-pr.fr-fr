---
description: 'En savoir plus sur : fonction JetOSSnapshotTruncateLogInstance'
title: JetOSSnapshotTruncateLogInstance fonction)
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da5c999f9fcec38878f339cfb2a927c2be2e5b70
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479025"
---
# <a name="jetossnapshottruncateloginstance-function"></a>JetOSSnapshotTruncateLogInstance fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetossnapshottruncateloginstance-function"></a>JetOSSnapshotTruncateLogInstance fonction)

La fonction **JetOSSnapshotTruncateLogInstance** tronque le journal pour une instance spécifiée pendant une session d’instantané.

**Windows vista :****JetOSSnapshotTruncateLogInstance** est introduit dans Windows vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*snapId*

Identificateur de la session d’instantané.

*instancié*

Instance qui sera utilisée pour cet appel.

*grbit*

Options pour cet appel. Ce paramètre peut avoir une combinaison des valeurs suivantes.

*Grbit* peut prendre l’une des valeurs suivantes :


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitAllDatabasesSnapshot</p> | <p>Toutes les bases de données sont attachées afin que le moteur de stockage puisse calculer et effectuer la troncation du journal.</p> | 
| <p>0 (zéro)</p> | <p>Aucune troncation ne se produit.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Le paramètre <em>Grbit</em> n’est pas valide.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>La session d’instantané n’est pas dans l’État dans lequel une troncation peut se produire. Les causes possibles sont :</p><ul><li><p>L’appel se termine après le délai d’expiration de la session d’instantané.</p></li><li><p>La session a été spécifiée en tant qu’instantané de copie.</p></li></ul> | 



Si cette fonction est réussie, les fichiers journaux d’une ou de toutes les instances qui font partie de la session d’instantané seront tronqués, si possible.

#### <a name="remarks"></a>Remarques

Cette fonction doit être appelée uniquement si l’instantané a été créé avec l’option JET_bitContinueAfterThaw. Dans le cas contraire, la session d’instantané se termine après l’appel à [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
