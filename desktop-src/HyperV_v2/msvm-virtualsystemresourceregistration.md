---
description: Inscrit un service qui fournit des objets liés aux ressources propres à l’ordinateur virtuel.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Classe Msvm_VirtualSystemResourceRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525186"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a>MSVM \_ VirtualSystemResourceRegistration, classe

Inscrit un service qui fournit des objets liés aux ressources propres à l’ordinateur virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualSystemResourceRegistration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualSystemResourceRegistration** possède les propriétés suivantes.

<dl> <dt>

**Composant**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de qui décrit l’objet COM qui implémente cette classe.

</dd> <dt>

**IsRootDevice**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si cette inscription indique si le type de ressource spécifié est l’appareil racine (ou sans parent) pour ce service ; Sinon, **false**. Une seule inscription peut exister lorsque **IsRootDevice** a la valeur **true**. Dans le cas contraire, cette inscription représente un mappage à un sous-appareil. La valeur de cette propriété est toujours **false**.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de qui décrit un type de ressource pris en charge par le service. Cette propriété est héritée de [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ VirtualSystemResourceRegistration** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Fin de la prise en charge des clients<br/>    | Windows 8.1<br/>                                                                                  |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualizationComponentRegistration**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

