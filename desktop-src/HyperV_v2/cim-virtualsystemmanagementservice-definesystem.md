---
description: Définit un système virtuel.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Méthode DefineSystem de la classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a18145a2b59e1ba93967ad7f1d529466dfc1e6ac094b74d139a36fbe6f77a57a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068639"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Méthode DefineSystem de la \_ classe CIM VirtualSystemManagementService

Définit un système virtuel.

L’entrée qui n’est pas complètement spécifiée peut être remplie avec des valeurs par défaut.

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

Chaîne contenant une instance incorporée de la classe [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) qui est utilisée pour définir les attributs du système virtuel à créer.

</dd> <dt>

*ResourceSettings* \[ dans\]
</dt> <dd>

Tableau de chaînes contenant chacune une instance incorporée de la classe [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) qui décrit les aspects virtuels d’une ressource virtuelle à créer dans l’étendue du nouveau système virtuel.

</dd> <dt>

*ReferenceConfiguration* \[ dans\]
</dt> <dd>

Référence à une instance d’objet [**\_ VirtualSystemSettingDat CIM**](cim-virtualsystemsettingdata.md) qui est l’objet de niveau supérieur d’une configuration de système virtuel de référence. La configuration de référence est utilisée pour compléter la configuration du nouveau système virtuel si les paramètres *SystemSettings* et *ResourceSettings* n’ont pas fourni les informations correspondantes.

</dd> <dt>

*ResultingSystem* \[ à\]
</dt> <dd>

Si un système d’ordinateur virtuel est correctement défini, une référence à une instance de la classe [**CIM CIM \_**](cim-computersystem.md) qui représente le système d’ordinateur virtuel nouvellement défini est retournée.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail. Dans ce cas, l’instance de la [**classe \_ CIM CIM**](cim-computersystem.md) qui représente le nouveau système virtuel est présentée par le biais de l’Association [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) avec la propriété **AffectedElement** qui fait référence à la nouvelle instance de la classe **CIM CIM \_** et à la propriété **ElementEffects** définie sur 5 (créer).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




