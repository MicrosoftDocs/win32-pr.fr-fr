---
description: 'En savoir plus sur : fonction JetOSSnapshotEnd'
title: JetOSSnapshotEnd fonction)
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b57528899b8d78ecee31f6dd54c2ac8decece383
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984432"
---
# <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd fonction)

La fonction **JetOSSnapshotEnd** informe le moteur que la session d’instantané est terminée.

**Windows vista :****JetOSSnapshotEnd** est introduit dans Windows vista :.  

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*snapId*

Identificateur de la session d’instantané.

*grbit*

Options pour cet appel. Ce paramètre peut avoir une combinaison des valeurs suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>0</p> | <p>Fin de la session d’instantané.</p> | 
| <p>JET_bitAbortSnapshot</p> | <p>La session d’instantané a été abandonnée.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>L’une des options demandées n’est pas valide, est utilisée de manière incorrecte ou n’est pas implémentée.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Une session d’instantané est déjà en cours. Cette opération n’est pas autorisée.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L’identificateur de la session d’instantané n’est pas valide.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>La session d’instantané avait un délai d’expiration interne avant l’appel de cet appel. Par conséquent, les opérations d’e/s retournées à normal avant cet appel ont été effectuées.</p> | 



Si cette fonction réussit, une session d’instantané se termine et le comportement normal du moteur reprendra. Une nouvelle session d’instantané peut être démarrée ultérieurement.

Si cette fonction échoue, le code de retour de la JET_errOSSnapshotTimeOut retourne et la session d’instantané en cours se termine, mais le gel d’IOs pendant la période de capture instantanée n’a pas été respecté en interne. Pour toutes les autres erreurs, l’état de la session d’instantané ne sera pas modifié.

#### <a name="remarks"></a>Remarques

Cette fonction est appelée uniquement si [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) a été appelé avec JET_bitContinueAfterThaw.

La session d’instantané doit se terminer pour que la vérification de l’instantané et la troncation du journal aient lieu. Les entrées du journal des événements seront générées pour les différentes étapes de l’instantané.

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
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
