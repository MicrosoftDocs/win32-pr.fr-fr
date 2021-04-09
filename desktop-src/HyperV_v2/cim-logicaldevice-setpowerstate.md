---
description: Définit l’état d’alimentation de l’appareil. L’utilisation de cette méthode est dépréciée. Utilisez plutôt la méthode SetPowerState dans la classe PowerManagementService associée.
ms.assetid: 2f53a8bd-18a8-45aa-92ad-68a33b6a42ab
title: Méthode SetPowerState de la classe CIM_LogicalDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a29f71806747e6d63f53618acd09d472ac8bdea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952523"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-hyper-v-management"></a>Méthode SetPowerState de la classe CIM_LogicalDevice (gestion Hyper-V)

Définit l’état d’alimentation de l’appareil. L’utilisation de cette méthode est dépréciée. Utilisez plutôt la méthode **SetPowerState** dans la classe **PowerManagementService** associée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PowerState* \[ dans\]
</dt> <dd>

État d’alimentation à définir.

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

**Pleine puissance** (1)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

Économie **d’énergie-mode faible puissance** (2)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

Économie **d’énergie-veille** (3)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

Économie **d’énergie-autres** (4)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Cycle d’alimentation** (5)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Mise hors tension** (6)


</dt> <dd></dd> </dl> </dd> <dt>

*Heure* \[ dans\]
</dt> <dd>

L’heure indique quand l’état de l’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

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

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




