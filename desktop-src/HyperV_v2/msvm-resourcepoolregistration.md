---
description: Inscrit un service qui fournit des objets liés aux pools de ressources globaux.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Classe Msvm_ResourcePoolRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bbcb0f2e3d5b0dfad884572c90f889d28e47fcffaf328b39d78f02d4c2baa3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535469"
---
# <a name="msvm_resourcepoolregistration-class"></a>MSVM \_ ResourcePoolRegistration, classe

Inscrit un service qui fournit des objets liés aux pools de ressources globaux.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ResourcePoolRegistration** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ResourcePoolRegistration** possède les propriétés suivantes.

<dl> <dt>

**Composant**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de qui décrit l’objet COM qui implémente cette classe.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à une instance de qui décrit un type de ressource pris en charge par le service. Cette propriété est héritée de [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ ResourcePoolRegistration** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
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

 

