---
description: Met à jour les paramètres d’un disque dur virtuel.
ms.assetid: 10f80313-bc78-447e-bdf2-5635d7354e3c
title: Méthode SetVirtualHardDiskSettingData de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3fb107edc5227cd5a3ff1f96f0e68c038fb00817cfb945dd08fcaea5d2254229
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050469"
---
# <a name="setvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a>Méthode SetVirtualHardDiskSettingData de la \_ classe ImageManagementService MSVM

Met à jour les paramètres d’un disque dur virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetVirtualHardDiskSettingData(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VirtualDiskSettingData* \[ dans\]
</dt> <dd>

Représentation sous forme de chaîne de la classe [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) qui spécifie le disque dur virtuel à mettre à jour et qui contient les nouvelles données de paramètre. Seules les propriétés **ParentPath**, **PhysicalSectorSize** ou **VirtualDiskId** peuvent être mises à jour avec cette méthode. Vous ne pouvez pas mettre à jour ces propriétés avec un appel de méthode. Vous pouvez uniquement mettre à jour l’une de ces propriétés à l’aide d’un seul appel de méthode.

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

**Fichier introuvable** (32779)
</dt> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

