---
description: Représente les paramètres d’un système virtuel à importer. Utilisé par la méthode demount de la \_ classe AssignableDeviceService MSVM.
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Classe Msvm_AssignableDeviceDismountSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67d2bf61cc317fee3dd04e464384020cfa04be9f601205e44d031c4fe4fa3ff8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693489"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a>MSVM \_ AssignableDeviceDismountSettingData, classe

Représente les paramètres d’un système virtuel à importer. Utilisé par la méthode [**demount**](msvm-assignabledeviceservice-dismountassignabledevice.md) de la [**classe \_ AssignableDeviceService MSVM**](msvm-assignabledeviceservice.md) .

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ AssignableDeviceDismountSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ AssignableDeviceDismountSettingData** possède les propriétés suivantes.

<dl> <dt>

**DeviceInstancePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

ID d’instance de périphérique PNP.

</dd> <dt>

**DeviceLocationPath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Chemin de l’emplacement de l’appareil PNP.

</dd> <dt>

**RequireAcsSupport**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si la prise en charge des services ACS requis doit être en place avant d’autoriser le démontage.

</dd> <dt>

**RequireDeviceMitigations**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si les atténuations d’appareil doivent être en place avant d’autoriser le démontage.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




