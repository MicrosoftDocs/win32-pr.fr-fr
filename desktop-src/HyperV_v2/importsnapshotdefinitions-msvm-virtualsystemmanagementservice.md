---
description: Recherche dans le dossier spécifié les fichiers de définition d’instantané associés au système informatique planifié spécifié et crée un nouvel instantané sur le système informatique planifié pour chaque fichier de définition associé à cet emplacement.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Méthode ImportSnapshotDefinitions de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cfa20eb845546f58201bdc167cfbe38bd4a3bd0ad327a04e009db4504ce0966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694589"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode ImportSnapshotDefinitions de la \_ classe VirtualSystemManagementService MSVM

Recherche dans le dossier spécifié les fichiers de définition d’instantané associés au système informatique planifié spécifié et crée un nouvel instantané sur le système informatique planifié pour chaque fichier de définition associé à cet emplacement.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PlannedSystem* \[ dans\]
</dt> <dd>

Référence à un objet [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) qui représente l’ordinateur virtuel planifié qui fait référence aux captures instantanées à importer.

</dd> <dt>

*SnapshotFolder* \[ dans\]
</dt> <dd>

Le chemin d’accès complet au dossier dans lequel se trouvent les configurations d’instantanés pour cet ordinateur virtuel.

</dd> <dt>

*ImportedSnapshots* \[ à\]
</dt> <dd>

Si l’opération se termine de façon synchrone, il s’agit d’un tableau de références aux instances [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) représentant les captures instantanées qui ont été correctement importées.

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

 

