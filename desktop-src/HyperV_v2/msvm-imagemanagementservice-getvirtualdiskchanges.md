---
description: Récupère une liste de modifications dans la région spécifiée d’un disque virtuel depuis l’ID de Change Tracking résilient fourni ou l’ID d’instantané VHDSet.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Méthode GetVirtualDiskChanges de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8b96c5b4d2bbdff78b6f9f2bc9a1e7547742a553564e0f81547b8d998f86f14f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522559"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a>Méthode GetVirtualDiskChanges de la \_ classe ImageManagementService MSVM

Récupère une liste de modifications dans la région spécifiée d’un disque virtuel depuis l’ID de Change Tracking résilient fourni ou l’ID d’instantané VHDSet.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* \[ dans\]
</dt> <dd>

Chemin d’accès complet qui spécifie l’emplacement du fichier de disque dur virtuel.

</dd> <dt>

*LimitId* \[ dans\]
</dt> <dd>

ID d’Change Tracking résilient ou ID d’instantané de définition de disque dur virtuel indiquant la ligne de base pour les modifications apportées au disque virtuel.

</dd> <dt>

*TargetSnapshotId* \[ dans\]
</dt> <dd>

ID d’instantané VHDSet indiquant la capture instantanée à comparer à la ligne de base lors de la détermination des modifications apportées au disque dur virtuel. Ce paramètre n’est valide que pour les fichiers de définition de VHD.

</dd> <dt>

*ByteOffset* \[ dans\]
</dt> <dd>

Décalage d’octet de la région du disque virtuel pour lequel interroger les modifications.

</dd> <dt>

*ByteLength* \[ dans\]
</dt> <dd>

Longueur en octets de la région du disque virtuel pour laquelle interroger les modifications. Cette valeur doit être inférieure à la taille du disque virtuel.

</dd> <dt>

*ProcessedByteLength* \[ à\]
</dt> <dd>

Longueur totale en octets traitée. Cette valeur peut être inférieure ou égale à ByteLength.

</dd> <dt>

*ChangedByteOffsets* \[ à\]
</dt> <dd>

Liste des décalages d’octets dans le disque virtuel indiquant le début de chaque plage modifiée.

</dd> <dt>

*ChangedByteLengths* \[ à\]
</dt> <dd>

Liste des longueurs d’octets des plages modifiées dans le disque virtuel.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence au travail (peut avoir la valeur null si la tâche est terminée).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l'une des valeurs suivantes :

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

**Fichier introuvable** (32779)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




