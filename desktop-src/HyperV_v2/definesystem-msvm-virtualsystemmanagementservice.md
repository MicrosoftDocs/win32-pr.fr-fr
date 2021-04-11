---
description: Crée une instance de machine virtuelle.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Méthode DefineSystem de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204025"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode DefineSystem de la \_ classe VirtualSystemManagementService MSVM

Crée une instance de machine virtuelle. Les propriétés qui ne sont pas spécifiées sont remplies avec les valeurs par défaut.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SystemSettings* \[ dans\]
</dt> <dd>

Type : **chaîne**

Une instance incorporée de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) utilisée pour définir les attributs de l’ordinateur virtuel à créer. Ce paramètre est obligatoire.

</dd> <dt>

*ResourceSettings* \[ dans\]
</dt> <dd>

Type : **chaîne \[ \]**

Nombre d’instances incorporées de la classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (ou classes dérivées de celles-ci). Ensemble, ces instances décrivent les ressources virtuelles de l’ordinateur virtuel. Un ensemble d’appareils par défaut sera créé pour l’ordinateur virtuel, que ce paramètre soit défini ou non. Par exemple, le processeur et la mémoire sont automatiquement créés et configurés avec les valeurs par défaut.

</dd> <dt>

*ReferenceConfiguration* \[ dans\]
</dt> <dd>

Type : **CIM \_ VirtualSystemSettingData**

Référence à une instance de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui est l’objet de niveau supérieur d’une configuration d’ordinateur virtuel de référence. La configuration de référence est utilisée pour compléter la configuration du nouvel ordinateur virtuel si les paramètres *SystemSettings* et *ResourceSettings* n’ont pas fourni d’informations respectives.

</dd> <dt>

*ResultingSystem* \[ à\]
</dt> <dd>

Type : **CIM \_ CIM**

Référence à une instance de la classe [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel nouvellement créé.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Type : **CIM \_ ConcreteJob**

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Si cette méthode est exécutée de façon synchrone, elle retourne 0 si elle réussit. Si cette méthode est exécutée de façon asynchrone, elle retourne 4096 et le paramètre de sortie de la *tâche* peut être utilisé pour suivre la progression de l’opération asynchrone. Toute autre valeur de retour indique une erreur.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Échec** (2)
</dt> <dt>

**Délai d’expiration** (3)
</dt> <dt>

**Paramètre non valide** (4)
</dt> <dt>

**DMTF réservé** (..)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Méthode réservée** (4097.. 32767)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
</dt> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

