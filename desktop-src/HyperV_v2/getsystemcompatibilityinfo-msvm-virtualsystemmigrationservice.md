---
description: Génère un blob opaque de données qui contient des informations de compatibilité pour le système spécifié.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Méthode GetSystemCompatibilityInfo de la classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4866b54bb6f5d5b90d4221b81e8a847e910e4486edc55eb4f932684397072504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392813"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Méthode GetSystemCompatibilityInfo de la \_ classe VirtualSystemMigrationService MSVM

Génère un blob opaque de données qui contient des informations de compatibilité pour le système spécifié. Cette méthode est utilisée conjointement avec la méthode [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) pour déterminer si une migration rapide ou dynamique d’un ordinateur virtuel vers un autre système d’ordinateur d’hébergement est possible sans réellement tenter la migration.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à une classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel pour lequel récupérer des informations de compatibilité. Si ce paramètre fait référence au système de l’ordinateur hôte, les données retournées dans le paramètre *CompatibilityInfo* peuvent être utilisées pour déterminer si l’un des ordinateurs virtuels sur le système informatique d’hébergement peut être rapidement migré vers un autre système informatique d’hébergement.

</dd> <dt>

*CompatibilityInfo* \[ à\]
</dt> <dd>

Un blob de données opaque qui peut être passé à la méthode [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) sur un autre système d’ordinateur hôte pour confirmer la compatibilité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




