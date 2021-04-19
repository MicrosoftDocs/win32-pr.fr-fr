---
description: Demande un changement d’État.
ms.assetid: 984e8a68-bc95-4a8b-99d6-ac248e96c45e
title: Méthode RequestStateChange de la classe Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9d3527f380bec783bd6305f2ec4fa57c15684dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514152"
---
# <a name="requeststatechange-method-of-the-msvm_synthetickeyboard-class"></a>Méthode RequestStateChange de la \_ classe MSVM SyntheticKeyboard

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

État demandé pour l’élément. Ces informations seront placées dans la propriété **RequestedState** de l’instance si le code de retour de la méthode RequestStateChange est 0 (terminé sans erreur») ou 4096 (0x1000) ('Job Started'). Reportez-vous à la description des propriétés **EnabledState** et **RequestedState** pour obtenir des explications détaillées sur les valeurs de *RequestedState* .

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

Peut contenir une référence au [**\_ ConcreteJob CIM**](cim-concretejob.md) créé pour effectuer le suivi de la transition d’État initiée par l’appel de méthode.

</dd> <dt>

*TimeoutPeriod* \[ dans\]
</dt> <dd>

Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État. Le format d’intervalle doit être utilisé pour spécifier le TimeoutPeriod. La valeur 0 ou un paramètre null indique que le client n’a aucune exigence de temps pour la transition.

Si cette propriété ne contient pas 0 ou null et que l’implémentation ne prend pas en charge ce paramètre, le code de retour « utilisation du paramètre de délai d’attente non pris en charge » doit être retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ; Sinon, retourne une erreur.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
</dt> </dl>

 

 




