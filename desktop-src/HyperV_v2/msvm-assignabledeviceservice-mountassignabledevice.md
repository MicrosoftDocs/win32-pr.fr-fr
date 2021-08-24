---
description: Monte l’appareil PCI spécifié afin qu’il puisse être utilisé par le système de l’ordinateur hôte.
ms.assetid: 2a07174e-c221-4c04-81b8-5968aa67e235
title: Méthode MountAssignableDevice de la classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.MountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: af7848306a289703717919f6e3407218774a8eba96814677cad9d7bf6f694aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790309"
---
# <a name="mountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a>Méthode MountAssignableDevice de la \_ classe AssignableDeviceService MSVM

Monte l’appareil PCI spécifié afin qu’il puisse être utilisé par le système de l’ordinateur hôte.

## <a name="syntax"></a>Syntaxe


```mof
uint32 MountAssignableDevice(
  [in]  string              DeviceInstancePath,
  [in]  string              DeviceLocationPath,
  [out] string              MountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DeviceInstancePath* \[ dans\]
</dt> <dd>

Chaîne contenant le chemin d’accès de l’instance d’appareil à un appareil.

</dd> <dt>

*DeviceLocationPath* \[ dans\]
</dt> <dd>

Chaîne contenant le chemin d’accès de l’emplacement de l’appareil à un appareil.

</dd> <dt>

*MountedDeviceInstancePath* \[ à\]
</dt> <dd>

Chaîne contenant le chemin d’accès à l’instance du périphérique monté.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence au travail (peut avoir la valeur null si la tâche est terminée).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.

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
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




