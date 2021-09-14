---
description: Le \_ SystemConfigurationChangeEvent Win32&\# 8194 ; La classe WMI indique que la liste des appareils a été actualisée sur le système (un appareil a été ajouté ou supprimé ou la configuration a été modifiée).
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Classe Win32_SystemConfigurationChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0bc479d3415906a6536c6df1d163056e94e2af76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999448"
---
# <a name="win32_systemconfigurationchangeevent-class"></a>\_Classe SystemConfigurationChangeEvent Win32

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemConfigurationChangeEvent** WMI indique que la liste des appareils sur le système a été actualisée (un appareil a été ajouté ou supprimé ou la configuration a été modifiée). Un événement est déclenché et une instance de cette classe est créée lorsque le message « DevMgrRefreshOn<*ComputerName*> » est envoyé. La modification exacte de la liste des appareils n’est pas contenue dans le message, de sorte qu’une actualisation de l’appareil est nécessaire pour obtenir les paramètres système actuels. Les paramètres IRQ, les ports COM et les versions du BIOS sont des exemples de modifications de configuration affectées.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SystemConfigurationChangeEvent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SystemConfigurationChangeEvent** a ces propriétés.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("messages de gestion Win32APIDevice \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice de gestion des messages \| WM \_ SETTINGCHANGE")
</dt> </dl>

Type de notification de modification d’événement qui s’est produite.

Cette propriété est héritée de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

**Configuration modifiée** (1)


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

**Arrivée** de l’appareil (2)


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

**Suppression** de l’appareil (3)


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

**Ancrage** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**descripteur de sécurité \_**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement. Cette propriété est héritée de l' [**\_ \_ événement**](../wmisdk/--event.md). Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](../wmisdk/wmi-security-constants.md).

</dd> <dt>

**HEURE de \_ création**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur unique qui indique l’heure à laquelle l’événement a été généré. Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601. Les informations sont au format de temps universel coordonné (UTC).

Cette propriété est héritée de l' [**\_ \_ événement**](../wmisdk/--event.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ SystemConfigurationChangeEvent** est dérivée de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_DeviceChangeEvent Win32**](win32-devicechangeevent.md)
</dt> <dt>

[Classes du système d’exploitation](./operating-system-classes.md)
</dt> </dl>

 

 
