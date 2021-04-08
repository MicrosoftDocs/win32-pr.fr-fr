---
description: Représente une association entre une instance de MSVM \_ GuestServiceInterfaceComponent et une instance de MSVM \_ GuestService, qui représente un service s’exécutant dans l’invité.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Classe Msvm_RegisteredGuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 850d7f081b070fd34ef11bc56e8cd1f914e498b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756892"
---
# <a name="msvm_registeredguestservice-class"></a>MSVM \_ RegisteredGuestService, classe

Représente une association entre une instance de [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) et une instance de [**MSVM \_ GuestService**](msvm-guestservice.md), qui représente un service s’exécutant dans l’invité. Cette classe dérive de la classe de [**\_ dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ RegisteredGuestService** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ RegisteredGuestService** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ dependency. Antecedent")
</dt> </dl>

Référence au composant de l’interface de service invité dans cette association.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ GuestService**](msvm-guestservice.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dépendance CIM \_ . dependent")
</dt> </dl>

Référence au service invité inscrit qui dépend de la propriété **Antecedent** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> <dt>

[**\_Dépendance CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

