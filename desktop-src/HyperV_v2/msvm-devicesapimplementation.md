---
description: 'Classe Msvm_DeviceSAPImplementation : association entre un point d’accès de service (SAP) et la façon dont il est implémenté.'
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Classe Msvm_DeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f5a8ccd02926d781f46ef86b26873c5dad86565ac90df47a5835cdf2ca4823a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525409"
---
# <a name="msvm_devicesapimplementation-class"></a>MSVM \_ DeviceSAPImplementation, classe

Association entre un point d’accès de service (SAP) et son implémentation. La cardinalité de cette association est plusieurs-à-plusieurs. Un SAP peut être fourni par plusieurs unités logiques, fonctionnant conjointement. N’importe quel appareil peut fournir plusieurs SAP. Lorsque de nombreux périphériques logiques sont associés à un seul SAP, il est supposé que ces éléments fonctionnent conjointement pour fournir le point d’accès. Si différentes implémentations d’un SAP existent, chacune de ces implémentations entraînerait des instanciations individuelles de l’objet SAP. Ces instanciations individuelles ont ensuite des associations avec les implémentations uniques.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ DeviceSAPImplementation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ DeviceSAPImplementation** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Unité logique. Cette propriété est héritée de la [**\_ DeviceSAPImplementation CIM**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM ( \_ ServiceAccessPoint** )](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Point d’accès au service implémenté à l’aide de l’unité logique. Cette propriété est héritée de la [**\_ DeviceSAPImplementation CIM**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ DeviceSAPImplementation** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemples

Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).

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

[**\_DEVICESAPIMPLEMENTATION CIM**](cim-devicesapimplementation.md)
</dt> <dt>

[**\_DEVICESAPIMPLEMENTATION CIM**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

