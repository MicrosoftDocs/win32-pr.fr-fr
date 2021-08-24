---
description: représente un élément de pool de ressources de la plateforme Microsoft Windows Hyper-V.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Classe Msvm_ResourcePoolComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 470317d3afd961ad74eb788ebdb70e67617749446fa4a432f40f00f43214cd92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535609"
---
# <a name="msvm_resourcepoolcomponent-class"></a>MSVM \_ ResourcePoolComponent, classe

représente un élément de pool de ressources de la plateforme Microsoft Windows Hyper-V.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ResourcePoolComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ResourcePoolComponent** possède les propriétés suivantes.

<dl> <dt>

**AllocationCapabilitiesClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe dérivée de [**la \_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) qui décrit les fonctionnalités d’allocation de ce pool de ressources.

</dd> <dt>

**IDENTIFICATEUR**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**GUID** qui représente l’identificateur de classe de l’objet com du service. Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Contexte**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Contexte dans lequel l’objet nouvellement créé s’exécutera. Cette valeur est passée dans le paramètre *dwClsContext* à **CoCreateInstance**. Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)et est toujours définie sur 1.

</dd> <dt>

**Activé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si cette instance est activée et peut être utilisée pour effectuer les demandes des clients ; Sinon, **false**. Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)et est toujours définie sur **true**.

</dd> <dt>

**MaxParentPools**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre maximal de pools de ressources parents pris en charge par un pool enfant.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Chaîne indépendante du langage qui identifie de façon unique l’élément. Le format suivant est suggéré pour empêcher les conflits de noms : « version du composant du fournisseur \| \| ». Par exemple, ce nom représente la version 1,0 du composant de port réseau émulé Microsoft : « Microsoft \| EmulatedNetworkPortComponent \| v 1.0 ». Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**PhysicalDeviceClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe dérivée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) qui implémente l’appareil physique à partir duquel ce pool alloue des ressources. Cette propriété peut avoir la **valeur null** si la classe d’appareil virtuel allouée à partir de ce pool est la même que la classe de l’appareil physique.

</dd> <dt>

**ResourcePoolClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe dérivée de [**la \_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)) qui implémente le pool de ressources.

</dd> <dt>

**ResourcePoolSettingDataClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la classe dérivée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) qui décrit les paramètres liés à la non-allocation du pool de ressources.

</dd> <dt>

**WmiFactoryCLSID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**GUID** qui représente l’identificateur de classe de la fabrique d’objets WMI du composant.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ ResourcePoolComponent** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

