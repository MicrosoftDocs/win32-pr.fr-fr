---
description: Définit l’association entre une extension de commutateur Ethernet installée et une extension de commutateur Ethernet.
ms.assetid: 306658ed-03a4-49fa-8704-f4b83a4bdd4f
title: Classe Msvm_ConcreteDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteDependency
- Msvm_ConcreteDependency.Antecedent
- Msvm_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d11908d98e4f7ef9cf84bc3622d801482ac7b33f767202ba4e739e8f4069178d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531719"
---
# <a name="msvm_concretedependency-class"></a>MSVM \_ ConcreteDependency, classe

Définit l’association entre une extension de commutateur Ethernet installée et une extension de commutateur Ethernet.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteDependency : CIM_ConcreteDependency
{
  Msvm_InstalledEthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension          REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ConcreteDependency** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ConcreteDependency** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) qui représente un composant d’extension de commutateur Ethernet virtuel installé sur le système.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) qui représente l’occurrence de l' **antécédent** lié à un commutateur Ethernet virtuel spécifique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

