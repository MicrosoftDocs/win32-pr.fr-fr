---
description: La méthode SetPowerState de la \_ classe LOGICALDEVICE CIM définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.
ms.assetid: 0d9678e0-a956-45d3-ac41-5c1604478fd7
ms.tgt_platform: multiple
title: Méthode SetPowerState de la classe CIM_LogicalDevice (fournisseurs WMI CIMWin32)
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
- CIMWin32.dll
ms.openlocfilehash: 23093858f034a128c08ac2c39343a51a1d73de229440b444d37e777e2b0d0ba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439439"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-cimwin32-wmi-providers"></a>Méthode SetPowerState de la classe CIM_LogicalDevice (fournisseurs WMI CIMWin32)

La méthode **SetPowerState** de la \_ classe LogicalDevice CIM définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

Valeur **ValueMap** qui spécifie l’état d’alimentation souhaité pour cet appareil logique.

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Pleine puissance** (1)


</dt> <dd>

Toute la puissance.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (2)


</dt> <dd>

Économie d’énergie en mode faible consommation d’énergie.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (3)


</dt> <dd>

Économie d’énergie en veille.

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>Économie **d’énergie-autres** (4)


</dt> <dd>

Économie d’énergie.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (5)


</dt> <dd>

Cycle d’alimentation.

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (6)


</dt> <dd>

Mise hors tension.

</dd> </dl> </dd> <dt>

*Heure* \[ dans\]
</dt> <dd>

Spécifie quand l’état d’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu). Lorsque le paramètre *PowerState* est égal à 5 (« Power cycle »), le paramètre *Time* indique quand l’appareil doit se rallumer. La mise hors tension est immédiate.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 (zéro) en cas de réussite, 1 (un) si la demande *PowerState* et *Time* spécifiée n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.

## <a name="remarks"></a>Remarques

Dans une sous-classe, l’ensemble des codes de retour possibles doit être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode. Les chaînes dans lesquelles le contenu **ValueMap** est traduit doivent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** . Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_LOGICALDEVICE CIM](setpowerstate-method-in-class-cim-logicaldevice.md)
</dt> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




