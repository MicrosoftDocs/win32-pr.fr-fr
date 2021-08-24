---
description: La méthode ModifyResourceSettings de la classe CIM_VirtualSystemManagementService-modifie les paramètres de ressource virtuelle.
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Méthode ModifyResourceSettings de la classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bc001d87a95e54682f6b6b4ffdecd3c53d3288b58a6dcb5b6e9a8a4d2dc528e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682729"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Méthode ModifyResourceSettings de la \_ classe CIM VirtualSystemManagementService

Modifie les paramètres de ressource virtuelle.

En cas d’application à des parties d’une configuration de système virtuel « en cours », les ressources d’effets secondaires du système virtuel actif peuvent être modifiées.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ResourceSettings* \[ dans\]
</dt> <dd>

Tableau de chaînes contenant chacune une instance incorporée de la classe [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) qui décrit les modifications apportées aux aspects virtuels d’une ressource virtuelle existante. Toutes les instances doivent avoir un **InstanceID** valide afin d’identifier le paramètre de ressource virtuelle à modifier.

</dd> <dt>

*ResultingResourceSettings* \[ à\]
</dt> <dd>

Tableau de références aux instances de la [**classe \_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) représentant les aspects virtuels des ressources virtuelles modifiées.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est exécutée à long terme, le cas échéant, une tâche est retournée. Dans ce cas, les instances de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) représentant les paramètres de ressource modifiés sont disponibles via l’Association **CIM \_ ConreteComponent** à partir de l’instance de la classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant la configuration du système virtuel affecté.

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

**État non valide** (5)
</dt> <dt>

**Paramètres incompatibles** (6)
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

 

 




