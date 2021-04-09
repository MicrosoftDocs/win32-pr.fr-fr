---
description: Contient un résumé des informations sur le système d’ordinateur virtuel spécifié.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Classe Msvm_ComputerSystemSummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862653"
---
# <a name="msvm_computersystemsummaryinformation-class"></a>MSVM \_ ComputerSystemSummaryInformation, classe

Contient un résumé des informations sur le système d’ordinateur virtuel spécifié.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ComputerSystemSummaryInformation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ComputerSystemSummaryInformation** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données **: \_ CIM CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Objet [**CIM \_ CIM**](cim-computersystem.md) qui est une instance dans la représentation normalisée de la ressource managée.

> [!Note]
>
> Type de données mis à niveau à partir de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) dans Windows 10, version 1703.

 

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ SummaryInformationBase**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« dépendant »)
</dt> </dl>

Instance de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) qui représente une vue dénormalisée ou agrégée de la ressource managée représentée par le [**MSVM \_ ComputerSystem**](msvm-computersystem.md) référencé par la propriété Antecedent.

> [!Note]
>
> Type de données mis à jour à partir de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) dans Windows 10, version 1703.

 

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

[**\_ELEMENTVIEW CIM**](cim-elementview.md)
</dt> </dl>

 

