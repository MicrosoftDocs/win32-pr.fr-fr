---
description: La \_ classe WMI de l’Association SerialPortSetting Win32 associe un port série et ses paramètres de configuration.
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Classe Win32_SerialPortSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234305"
---
# <a name="win32_serialportsetting-class"></a>\_Classe SerialPortSetting Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ SerialPortSetting Win32** associe un port série et ses paramètres de configuration.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SerialPortSetting** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SerialPortSetting** a ces propriétés.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ SerialPort**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")
</dt> </dl>

Un [**\_ SerialPort Win32**](win32-serialport.md) qui contient les propriétés d’un port série sur le système informatique.

</dd> <dt>

**Paramètre**
</dt> <dd> <dl> <dt>

Type de données : **Win32 \_ SerialPortConfiguration**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPortConfiguration")
</dt> </dl>

[**\_ SerialPortConfiguration Win32**](win32-serialportconfiguration.md) qui contient le paramètre de configuration pour le port série.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **Win32 \_ SerialPortSetting** est dérivée de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).

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

[**\_DeviceSettings Win32**](win32-devicesettings.md)
</dt> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> </dl>

 

 
