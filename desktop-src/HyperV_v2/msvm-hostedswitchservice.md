---
description: Association qui connecte un service de commutateur virtuel à un service de pontage transparent.
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Classe Msvm_HostedSwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0b7319dbe58649ac7abce2d36201f3984c1b807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516422"
---
# <a name="msvm_hostedswitchservice-class"></a>MSVM \_ HostedSwitchService, classe

Association qui connecte un service de commutateur virtuel à un service de pontage transparent.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ HostedSwitchService** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ HostedSwitchService** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) qui représente le commutateur virtuel.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **\_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) qui représente le service de pontage.

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ HostedSwitchService** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_Service hébergé CIM**](cim-hostedservice.md)
</dt> <dt>

[**\_Service hébergé CIM**](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

