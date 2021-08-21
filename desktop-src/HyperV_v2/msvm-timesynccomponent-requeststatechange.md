---
description: Méthode RequestStateChange de la classe Msvm_TimeSyncComponent-demande un changement d’État.
ms.assetid: ca014a24-1d16-468d-bc9c-8043249dabe2
title: Méthode RequestStateChange de la classe Msvm_TimeSyncComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c616fa06f02807e31ae5e58910bea1c9900c467186f6ec5943954198cd73c9f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811809"
---
# <a name="requeststatechange-method-of-the-msvm_timesynccomponent-class"></a>Méthode RequestStateChange de la \_ classe MSVM TimeSyncComponent

Demande un changement d’État.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RequestedState* \[ dans\]
</dt> <dd>

Nouvel état. Les informations sont placées dans la propriété **RequestedState** de l’instance si le code de retour de la méthode **RequestStateChange** est 0 ou 4096. Pour plus d’informations, consultez la description des propriétés **EnabledState** et **RequestedState** de l’élément. Il doit s’agir de l’une des valeurs suivantes.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Arrêter** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Hors connexion** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Test** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Différer** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Suspension** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Redémarrer** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Réinitialiser** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Peut contenir une référence au ConcreteJob créé pour effectuer le suivi de la transition d’État initiée par l’appel de méthode.

</dd> <dt>

*TimeoutPeriod* \[ dans\]
</dt> <dd>

Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État. Le format d’intervalle doit être utilisé pour spécifier le TimeoutPeriod. La valeur 0 ou un paramètre null indique que le client n’a aucune exigence de temps pour la transition.

Si cette propriété ne contient pas 0 ou null et que l’implémentation ne prend pas en charge ce paramètre, le code de retour « utilisation du paramètre de délai d’attente non pris en charge » doit être retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l'une des valeurs suivantes :

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ TimeSyncComponent**](msvm-timesynccomponent.md)
</dt> </dl>

 

 




