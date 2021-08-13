---
description: Ajoute des ressources à une configuration de système virtuel.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Méthode AddResourceSettings de la classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0387d3d46723aede1d0858d647a555db57b3de28e6c1fb5fbb68b6d56342fcb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646467"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Méthode AddResourceSettings de la \_ classe CIM VirtualSystemManagementService

Ajoute des ressources à une configuration de système virtuel.

En cas d’application à une configuration de système virtuel « État », des ressources d’effet secondaire sont ajoutées au système virtuel actif.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AffectedConfiguration* \[ dans\]
</dt> <dd>

Référence [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) à la configuration du système virtuel affecté.

</dd> <dt>

*ResourceSettings* \[ dans\]
</dt> <dd>

Tableau de chaînes contenant chacune une instance incorporée de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) qui décrit les aspects virtuels d’une ressource virtuelle à ajouter au système virtuel.

</dd> <dt>

*ResultingResourceSettings* \[ à\]
</dt> <dd>

Tableau de références aux instances de la [**classe \_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) représentant les aspects virtuels des ressources virtuelles ajoutées.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail. Dans ce cas, les instances de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) représentant les paramètres de ressource ajoutés sont disponibles par le biais de l’Association **CIM \_ ConreteComponent** à partir de l’instance de la classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant la configuration du système virtuel concerné.

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

 

 




