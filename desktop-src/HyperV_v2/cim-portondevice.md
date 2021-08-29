---
description: Représente une association entre un port ou un point de connexion et un appareil.
ms.assetid: b35e741a-7110-4e48-a132-d436f4fbf038
title: Classe CIM_PortOnDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PortOnDevice
- CIM_PortOnDevice.Antecedent
- CIM_PortOnDevice.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c58176d918c1faf8319c9953a3476e991c6d04b25629909407759cb01cbe1b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981269"
---
# <a name="cim_portondevice-class"></a>\_Classe CIM PortOnDevice

Représente une association entre un port ou un point de connexion et un appareil.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_PortOnDevice : CIM_HostedDependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ PortOnDevice** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ PortOnDevice** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ LogicalDevice CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Périphérique qui comprend le port.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ LogicalPort**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Port sur l’appareil.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_HOSTEDDEPENDENCY CIM**](cim-hosteddependency.md)
</dt> </dl>

 

