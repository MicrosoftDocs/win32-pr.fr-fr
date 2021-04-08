---
description: Associe le \_ VirtualSystemReferencePoint MSVM aux objets MSVM \_ VirtualSystem correspondants.
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Classe Msvm_ReferencePointOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debe1931154c5c7a7868e8ee301daf977076b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756897"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a>MSVM \_ ReferencePointOfVirtualSystem, classe

Associe [**le \_ VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md) aux objets [**MSVM \_ VirtualSystem**](msvm-virtualsystemresourcecomponent.md) correspondants.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ReferencePointOfVirtualSystem** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ReferencePointOfVirtualSystem** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ ComputerSystem**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’objet indépendant dans cette association.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ VirtualSystemReferencePoint**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »)
</dt> </dl>

[**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) qui représente l’objet dépendant de l' **antécédent**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> </dl>

 

