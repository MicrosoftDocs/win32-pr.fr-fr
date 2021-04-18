---
description: Demande que l’état du système planifié soit remplacé par la valeur spécifiée.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Méthode RequestStateChange de la classe Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519098"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a>Méthode RequestStateChange de la \_ classe MSVM PlannedComputerSystem

Demande que l’état du système planifié soit remplacé par la valeur spécifiée.

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

État demandé pour le système planifié.

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

Ce paramètre n’est pas utilisé et doit avoir la **valeur null**.

</dd> <dt>

*TimeoutPeriod* \[ dans\]
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                      | Description                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt></dt> <dt>0</dt> </dl>     | Succès<br/>                                                                 |
| <dl> <dt></dt><dt>4096</dt> </dl>  |                                                                                    |
| <dl> <dt></dt><dt>32768</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32769</dt> </dl> | Accès refusé.<br/>                                                          |
| <dl> <dt></dt><dt>32770</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32771</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32772</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32773</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32774</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32775</dt> </dl> | La valeur spécifiée dans le paramètre *RequestedState* n’est pas prise en charge.<br/> |
| <dl> <dt></dt><dt>32776</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32777</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32778</dt> </dl> |                                                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




