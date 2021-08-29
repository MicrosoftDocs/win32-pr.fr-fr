---
description: Demande que l’état du composant d’interface de service invité soit remplacé par la valeur spécifiée.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: 'Msvm_GuestServiceInterfaceComponent :: RequestStateChange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2b04859406a2600650caa1d822215291a84656d6909740008c2a87a9787f87a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501009"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a>MSVM \_ GuestServiceInterfaceComponent :: RequestStateChange, méthode

Demande que l’état du composant d’interface de service invité soit remplacé par la valeur spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RequestedState* \[ dans\]
</dt> <dd>

Type : **UInt16**

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

Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Référence facultative à un objet [**\_ ConcreteJob MSVM**](msvm-concretejob.md) qui est retourné si l’opération est exécutée de façon asynchrone. Si elle est présente, la référence retournée peut être utilisée pour surveiller la progression et obtenir le résultat de la méthode.

</dd> <dt>

*TimeoutPeriod* \[ dans\]
</dt> <dd>

Type : **DateTime**

Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État. Le format d’intervalle doit être utilisé pour spécifier le délai d’attente. La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition. Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                                                                       | Description         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Terminé sans erreur**</dt> <dt>0</dt> </dl>                           | Réussite.<br/> |
| <dl> <dt>**Non pris en charge**</dt> <dt>1</dt> </dl>                                     |                     |
| <dl> <dt>**Erreur 2 inconnue/non spécifiée**</dt> <dt></dt> </dl>                         |                     |
| <dl> <dt>**Impossible de se terminer dans le délai d’expiration**</dt> <dt>3</dt> </dl>            |                     |
| <dl> <dt>**Échec**</dt> <dt>4</dt> </dl>                                            |                     |
| <dl> <dt>**Paramètre non valide**</dt> <dt>5</dt> </dl>                                 |                     |
| <dl> <dt>**En cours d’utilisation**</dt> <dt>6</dt> </dl>                                            |                     |
| <dl> <dt>**DMTF réservé**</dt> <dt>..</dt> </dl>                                    |                     |
| <dl> <dt>**Paramètres de méthode vérifiés-transition démarrée**</dt> <dt>4096</dt> </dl> |                     |
| <dl> <dt>**Transition d’État non valide**</dt> <dt>4097</dt> </dl>                       |                     |
| <dl> <dt>**Utilisation du paramètre timeout non prise en charge**</dt> <dt>4098</dt> </dl>         |                     |
| <dl> <dt>**Occupé**</dt> <dt>4099</dt> </dl>                                           |                     |
| <dl> <dt>**Méthode réservée**</dt> <dt>4100.. 32767</dt> </dl>                         |                     |
| <dl> <dt></dt> <dt>32 768.. 65535</dt> spécifiques au fournisseur </dl>                        |                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\\\\\Virtualisation racine \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

