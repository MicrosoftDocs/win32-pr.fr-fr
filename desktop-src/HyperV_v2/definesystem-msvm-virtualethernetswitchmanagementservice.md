---
description: Crée un commutateur virtuel.
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Méthode DefineSystem de la classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867077"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Méthode DefineSystem de la \_ classe VirtualEthernetSwitchManagementService MSVM

Crée un commutateur virtuel. Les propriétés qui ne sont pas spécifiées sont remplies avec les valeurs par défaut.

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

Une instance incorporée de la classe [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) utilisée pour définir les attributs du commutateur virtuel à créer. Ce paramètre est obligatoire.

</dd> <dt>

*ResourceSettings* \[ dans\]
</dt> <dd>

Tableau d’instances incorporées de la classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) qui décrit les paramètres des ports de commutateur à créer dans l’étendue du nouveau commutateur virtuel. Si la **valeur null** est spécifiée, le commutateur virtuel est créé sans aucune ressource (c’est-à-dire aucun port de commutateur).

</dd> <dt>

*ReferenceConfiguration* \[ dans\]
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*ResultingSystem* \[ à\]
</dt> <dd>

Si un commutateur virtuel est créé avec succès, référence à une instance de la classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) qui représente le commutateur virtuel nouvellement défini.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

