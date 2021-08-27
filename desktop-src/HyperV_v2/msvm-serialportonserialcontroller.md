---
description: Associe un port série à un contrôleur série.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Classe Msvm_SerialPortOnSerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ddc5a5c006b92945178f89cf5f4df585f96ed3eaef692b04326878cb0d16520
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107439"
---
# <a name="msvm_serialportonserialcontroller-class"></a>MSVM \_ SerialPortOnSerialController, classe

Associe un port série à un contrôleur série.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SerialPortOnSerialController** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SerialPortOnSerialController** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Contrôleur série auquel le port est connecté. Cette propriété est héritée de la [**\_ PortOnDevice CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Port du contrôleur série. Cette propriété est héritée de la [**\_ PortOnDevice CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ SerialPortOnSerialController** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_PORTONDEVICE CIM**](cim-portondevice.md)
</dt> <dt>

[**\_PORTONDEVICE CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[Classes d’appareils série](serial-devices-classes.md)
</dt> </dl>

 

