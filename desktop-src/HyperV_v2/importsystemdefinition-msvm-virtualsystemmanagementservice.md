---
description: Crée un système informatique planifié basé sur la définition d’ordinateur virtuel spécifiée.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Méthode ImportSystemDefinition de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee8dd5bb7d17684216b747717c0adf32011dafa543f05c91a0c1264da89caf2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149735"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode ImportSystemDefinition de la \_ classe VirtualSystemManagementService MSVM

Crée un système informatique planifié basé sur la définition d’ordinateur virtuel spécifiée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SystemDefinitionFile* \[ dans\]
</dt> <dd>

Le chemin d’accès complet au fichier de définition de système (.xml ou. exp) représentant l’ordinateur virtuel à importer. Le fichier de définition ne doit pas être déjà utilisé par le système hôte ou la plateforme de virtualisation.

</dd> <dt>

*SnapshotFolder* \[ dans\]
</dt> <dd>

Le chemin d’accès complet au dossier dans lequel se trouvent les configurations d’instantanés pour cet ordinateur virtuel. Ce dossier sera recherché afin de localiser les captures instantanées référencées par la définition de la machine virtuelle. Les captures instantanées référencées introuvables à cet emplacement doivent être supprimées à l’aide de la méthode [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) , ou importées à l’aide de la méthode [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) avant de réaliser le système informatique planifié.

</dd> <dt>

*GenerateNewSystemIdentifier* \[ dans\]
</dt> <dd>

Indique s’il faut réutiliser l’identificateur unique de l’ordinateur virtuel. Si ce paramètre a la **valeur true**, un nouvel identificateur du système est généré. Si ce paramètre a la **valeur false**, l’identificateur système existant est utilisé.

</dd> <dt>

*ImportedSystem* \[ à\]
</dt> <dd>

Si l’opération se termine de façon synchrone, il s’agit d’une référence à un objet [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) qui représente la machine virtuelle importée.

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
</dt> <dt>

**Fichier en cours d’utilisation** (32779)
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

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

