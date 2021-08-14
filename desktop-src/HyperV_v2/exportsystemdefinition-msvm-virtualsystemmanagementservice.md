---
description: Exporte un ordinateur virtuel, ou un instantané d’un ordinateur virtuel, vers un fichier.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Méthode ExportSystemDefinition de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 72198055a81ce13a6b38859ed5ba6370faf7de046bc9f2cc3a158548c2679685
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254033"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode ExportSystemDefinition de la \_ classe VirtualSystemManagementService MSVM

Exporte un ordinateur virtuel, ou un instantané d’un ordinateur virtuel, vers un fichier. L’ordinateur virtuel doit être dans l’état « hors tension » ou « enregistré » pour être exporté. L’ordinateur virtuel, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à un [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel à exporter.

</dd> <dt>

*ExportDirectory* \[ dans\]
</dt> <dd>

Chemin d’accès complet du répertoire dans lequel l’ordinateur virtuel doit être exporté. Si la propriété **CreateVmExportSubdirectory** de la [**classe \_ VirtualSystemExportSettingData MSVM**](msvm-virtualsystemexportsettingdata.md) dans le paramètre *ExportSettingData* est définie sur **true**, ce répertoire peut être réutilisé pour l’exportation de plusieurs ordinateurs virtuels et cette méthode place chaque définition d’ordinateur virtuel dans un sous-répertoire distinct sous ce chemin d’accès.

</dd> <dt>

*ExportSettingData* \[ dans\]
</dt> <dd>

Instance incorporée de la classe [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) qui représente les paramètres de l’opération d’exportation.

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

 

