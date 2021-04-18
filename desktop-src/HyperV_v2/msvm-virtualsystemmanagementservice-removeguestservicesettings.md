---
description: Supprime les paramètres de service invité d’une configuration de système virtuel.
ms.assetid: 33e55d74-adfd-4174-8f05-14e797a33806
title: Méthode RemoveGuestServiceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0aee1f8f9d729c093bff2a580e054d93fa7fc033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533589"
---
# <a name="removeguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode RemoveGuestServiceSettings de la \_ classe VirtualSystemManagementService MSVM

Supprime les paramètres de service invité d’une configuration de système virtuel.

En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoveGuestServiceSettings(
  [in]  CIM_SettingData REF GuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*GuestServiceSettings* \[ dans\]
</dt> <dd>

Référence à un tableau de [**\_ SettingData CIM**](cim-settingdata.md) qui décrit le paramètre de service invité à supprimer.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l'une des valeurs suivantes :

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

