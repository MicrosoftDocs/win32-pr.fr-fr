---
description: Demande que l’état de la tâche de migration passe à l’état spécifié.
ms.assetid: f0be5ea8-7e21-407e-b84d-8bd4ca5a6a2c
title: Méthode RequestStateChange de la classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a7a5934049860e92aa9986a301fe3d75bed8022bda064653ee9e405ad16f6619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014317"
---
# <a name="requeststatechange-method-of-the-msvm_migrationjob-class"></a>Méthode RequestStateChange de la \_ classe MSVM MigrationJob

Demande que l’état de la tâche de migration passe à l’état spécifié. L’appel de la méthode **RequestStateChange** plusieurs fois peut entraîner le remplacement ou la perte des demandes antérieures. Si la valeur 0 est retournée, la tâche s’est terminée correctement. Tout autre code de retour indique une condition d’erreur.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RequestedState* \[ dans\]
</dt> <dd>

Nouvel état d’un travail.

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Démarrer** (2)


</dt> <dd>

Passe l’État à « en cours d’exécution ».

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (3)


</dt> <dd>

Arrête temporairement le travail. L’objectif est de redémarrer ensuite le travail avec « Start ». Il peut être possible d’entrer dans l’État « service » en suspens. (Il s’agit d’un travail spécifique.)

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminer** (4)


</dt> <dd>

Arrête le travail proprement dit, en enregistrant les données, en conservant l’État et en arrêtant tous les processus sous-jacents de manière ordonnée.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Met immédiatement fin à la tâche, sans qu’il soit nécessaire d’enregistrer les données ou de conserver l’État.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)


</dt> <dd>

Place le travail dans un état de service spécifique au fournisseur. Il peut être possible de redémarrer le travail.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF, réservé**


</dt> <dd>

Réservé.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé**


</dt> <dd>

Réservé.

</dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ dans\]
</dt> <dd>

Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État. Le format d’intervalle doit être utilisé pour spécifier le délai d’attente. La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition. Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (utilisation du paramètre timeout non pris en charge) doit être retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

<dl> <dt>

  (0)
</dt> <dt>

 (32768)
</dt> <dt>

 (32769)
</dt> <dt>

 (32770)
</dt> <dt>

 (32771)
</dt> <dt>

 (32772)
</dt> <dt>

 (32773)
</dt> <dt>

 (32774)
</dt> <dt>

 (32775)
</dt> <dt>

 (32776)
</dt> <dt>

 (32777)
</dt> <dt>

 (32778)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ MigrationJob**](msvm-migrationjob.md)
</dt> </dl>

 

 




