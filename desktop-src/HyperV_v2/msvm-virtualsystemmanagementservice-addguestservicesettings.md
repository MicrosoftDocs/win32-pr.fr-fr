---
description: Ajoute des paramètres de service invité à une configuration de système virtuel.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Méthode AddGuestServiceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5bcdfd8c159e92efe633c04e22af5bceb9d003e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525209"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode AddGuestServiceSettings de la \_ classe VirtualSystemManagementService MSVM

Ajoute des paramètres de service invité à une configuration de système virtuel.

En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AffectedConfiguration* \[ dans\]
</dt> <dd>

Référence à un [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) qui décrit la configuration affectée.

</dd> <dt>

*GuestServiceSettings* \[ dans\]
</dt> <dd>

Tableau contenant les paramètres du service invité.

</dd> <dt>

*ResultingGuestServiceSettings* \[ à\]
</dt> <dd>

En cas de réussite, contient une référence à un [**\_ SettingData CIM**](cim-settingdata.md) qui décrit les paramètres de service invité résultants.

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

**Non pris en charge** (1)
</dt> <dt>

**Échec** (2)
</dt> <dt>

**Délai d’expiration** (3)
</dt> <dt>

**Paramètre non valide** (4)
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

 

