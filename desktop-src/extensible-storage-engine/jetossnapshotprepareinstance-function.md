---
description: 'En savoir plus sur : fonction JetOSSnapshotPrepareInstance'
title: JetOSSnapshotPrepareInstance fonction)
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4140a79428c7db6cb9091627ae1aeb7416e6686
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988932"
---
# <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetossnapshotprepareinstance-function"></a>JetOSSnapshotPrepareInstance fonction)

La fonction **JetOSSnapshotPrepareInstance** sélectionne une instance spécifique pour faire partie de la session d’instantané.

**Windows vista :** **JetOSSnapshotPrepareInstance** a été introduit dans Windows vista.

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
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

Options pour cet appel. Ce paramètre est réservé à un usage futur. La seule valeur valide est 0 (zéro).

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Le pointeur d’ID d’instantané a la <strong>valeur null</strong> ou le paramètre <em>Grbit</em> n’est pas valide.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Une session d’instantané est déjà en cours.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L’identificateur de la session d’instantané n’est pas valide.</p> | 



Si cette fonction est réussie, l’instance spécifiée fera partie de la session d’instantané.

Si cette fonction échoue, aucune modification de l’état du moteur ne se produit.

#### <a name="remarks"></a>Remarques

L’appel de séquence d’API normal est : [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), éventuellement suivi d’un ou plusieurs appels à **JetOSSnapshotPrepareInstance**, puis de [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Une fois le blocage démarré, il peut être arrêté à l’aide de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md). À tout moment après la préparation, la session d’instantané peut être interrompue soudainement avec [JetOSSnapshotAbort](./jetossnapshotabort-function.md). Les entrées du journal des événements seront générées pour les différentes étapes de l’instantané.

Si **JetOSSnapshotPrepareInstance** n’est pas appelé entre le début de la session ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) et le moment du blocage ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), toutes les instances en cours d’exécution dans le moteur se figeront et feront partie de la session d’instantané. Cela se produit pour deux raisons :

  - Il simplifie le code pour les utilisateurs qui souhaitent toutes les instances.

  - Il permet la compatibilité descendante pour les appelants des API d’instantané.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
