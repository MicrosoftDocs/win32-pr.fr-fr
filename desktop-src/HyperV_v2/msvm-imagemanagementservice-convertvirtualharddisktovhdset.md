---
description: Convertit un fichier de disque dur virtuel en créant un nouveau fichier de définition de disque dur virtuel en même temps que le disque dur virtuel existant.
ms.assetid: 04ae723e-e3c5-4640-a0e5-0e1b75bb2e6d
title: Méthode ConvertVirtualHardDiskToVHDSet de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDiskToVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a54970529f51b3d616cd3c44676c0ffa91d31489f5b07f72a279a2ed8db008d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522779"
---
# <a name="convertvirtualharddisktovhdset-method-of-the-msvm_imagemanagementservice-class"></a>Méthode ConvertVirtualHardDiskToVHDSet de la \_ classe ImageManagementService MSVM

Convertit un fichier de disque dur virtuel en créant un nouveau fichier de définition de disque dur virtuel en même temps que le disque dur virtuel existant.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ConvertVirtualHardDiskToVHDSet(
  [in]  string              VirtualHardDiskPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VirtualHardDiskPath* \[ dans\]
</dt> <dd>

Chaîne contenant le chemin d’accès au fichier de disque dur virtuel. Le nouveau fichier de définition de disque dur virtuel aura le même nom de fichier, mais avec le. Extension de disques durs virtuels.

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

 

 




