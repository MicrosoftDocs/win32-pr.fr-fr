---
description: Obtient une liste d' \_ instances MSVM CompatibilityVector qui peuvent être utilisées pour vérifier la compatibilité de l’ordinateur virtuel (VM).
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Msvm_VirtualSystemMigrationService :: GetSystemCompatibilityVectors, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950998"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a>MSVM \_ VirtualSystemMigrationService :: GetSystemCompatibilityVectors, méthode

Obtient une liste d’instances [**MSVM \_ CompatibilityVector**](msvm-compatibilityvector.md) qui peuvent être utilisées pour vérifier la compatibilité de l’ordinateur virtuel (VM).

## <a name="syntax"></a>Syntaxe


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à une classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente la machine virtuelle pour laquelle récupérer des vecteurs de compatibilité. Si ce paramètre fait référence au système de l’ordinateur hôte, les données retournées dans le paramètre *CompatibilityVectors* peuvent être utilisées pour déterminer si l’une des machines virtuelles sur le système de l’ordinateur hôte peut être rapidement migrée vers un autre système informatique d’hébergement.

</dd> <dt>

*CompatibilityVectors* \[ à\]
</dt> <dd>

Tableau d’instances [**MSVM \_ CompatibilityVector**](msvm-compatibilityvector.md) qui contiennent les informations de compatibilité pour les machines virtuelles ou le système informatique d’hébergement.

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

## <a name="remarks"></a>Notes

**GetSystemCompatibilityVectors** obtient les informations de compatibilité d’un ordinateur virtuel (en cas d’exécution sur un système informatique d’ordinateur virtuel) ou d’un ordinateur hôte (en cas d’exécution sur un système d’ordinateur hôte). Les informations de compatibilité restent opaques pour le client, tandis que les informations permettent de comparer les informations de compatibilité de l’ordinateur hôte avec celles de la machine virtuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\\\\\Virtualisation racine \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ CompatibilityVector**](msvm-compatibilityvector.md)
</dt> <dt>

[**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




