---
description: Crée une capture instantanée d’un système virtuel.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Méthode CreateSnapshot de la classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ee1a2e66745ceac50cc00ba6e625a171f18c7d2b54d4e51af2c86f6711675ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532749"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>Méthode CreateSnapshot de la \_ classe CIM VirtualSystemSnapshotService

Crée une capture instantanée d’un système virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AffectedSystem* \[ dans\]
</dt> <dd>

Référence [**CIM \_ CIM**](cim-computersystem.md) au système virtuel affecté.

</dd> <dt>

*SnapshotSettings* \[ dans\]
</dt> <dd>

Paramètres.

</dd> <dt>

*SnapshotType* \[ dans\]
</dt> <dd>

Type d’instantané demandé :

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Instantané complet** (2)


</dt> <dd>

Capture instantanée complète du système virtuel.

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Capture instantanée de disque** (3)


</dt> <dd>

Capture instantanée des disques système virtuels.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Spécifique au fournisseur** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshot* \[ in, out\]
</dt> <dd>

Référence [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) à l’instantané du système virtuel résultant.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail. Dans ce cas, l’instance de la [**classe CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) représentant le nouvel instantané du système virtuel est présentée via l’Association [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) , avec la valeur de la propriété **AffectedElement** qui fait référence à la nouvelle instance de la classe **CIM \_ VirtualSystemSettingData** représentant l’instantané du système virtuel et la valeur de la **ElementEffects** définie à 5 (créer).

> [!Note]  
> Ce paramètre a été en lecture/écriture dans Windows 8.1.

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ; Sinon, retourne une erreur.

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

**Type non valide** (6)
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

[**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




