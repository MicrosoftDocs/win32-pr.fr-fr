---
description: Représente l’état du port PCI Express.
ms.assetid: 15d670ee-940a-4737-b2cd-e89dd8a63a5c
title: Classe Msvm_PciExpress
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpress
- Msvm_PciExpress.DeviceInstancePath
- Msvm_PciExpress.LocationPath
- Msvm_PciExpress.FunctionNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db30d367cbecd0e7b235000a35da26f5baaa07f1c05d0160a9b0bb23c7cfc2c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117811209"
---
# <a name="msvm_pciexpress-class"></a>MSVM \_ PciExpress, classe

Représente l’état du port PCI Express.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpress : CIM_LogicalDevice
{
  string DeviceInstancePath;
  string LocationPath;
  uint16 FunctionNumber;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ PciExpress** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ PciExpress** possède les propriétés suivantes.

<dl> <dt>

**DeviceInstancePath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne contenant le chemin d’accès à l’instance d’appareil qui identifie le périphérique PCI Express virtuel de l’appareil.

</dd> <dt>

**FunctionNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de fonction de l’appareil PCI Express virtuel.

</dd> <dt>

**LocationPath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne contenant le chemin d’accès à l’emplacement de l’appareil qui identifie le périphérique PCI Express virtuel de l’appareil.

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

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




