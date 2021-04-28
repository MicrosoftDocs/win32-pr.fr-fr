---
description: Méthode RemoveResourceSettings de la classe CIM_VirtualSystemManagementService-supprime les paramètres de ressources virtuelles d’une configuration de système virtuel.
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Méthode RemoveResourceSettings de la classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5c7daabcdcd732c3a5693664e1768ebf66668d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112257"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Méthode RemoveResourceSettings de la \_ classe CIM VirtualSystemManagementService

Supprime les paramètres de ressources virtuelles d’une configuration de système virtuel.

En cas d’application à des parties d’une configuration de système virtuel « en cours », les ressources d’effets secondaires du système virtuel actif peuvent être supprimées.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ResourceSettings* \[ dans\]
</dt> <dd>

Tableau de références aux instances de la classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) où chaque instance représente les paramètres d’une ressource virtuelle au sein d’une configuration de système virtuel qui doit être supprimée.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

 

 




