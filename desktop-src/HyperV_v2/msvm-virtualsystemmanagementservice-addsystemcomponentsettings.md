---
description: Ajoute des paramètres génériques à une configuration de système virtuel.
ms.assetid: ae04be39-0401-43e9-b19b-3539ca1786ec
title: Méthode AddSystemComponentSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56ca8bed752bab52f6a82e18975dd5df72dbe12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515412"
---
# <a name="addsystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode AddSystemComponentSettings de la \_ classe VirtualSystemManagementService MSVM

Ajoute des paramètres génériques à une configuration de système virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddSystemComponentSettings(
  [in]  Msvm_VirtualSystemSettingData   REF AffectedConfiguration,
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AffectedConfiguration* \[ dans\]
</dt> <dd></dd> <dt>

*ComponentSettings* \[ dans\]
</dt> <dd>

Paramètres du composant à ajouter.

</dd> <dt>

*ResultingComponentSettings* \[ à\]
</dt> <dd>

En cas de réussite, fait référence à un [**MSVM \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) qui contient les paramètres de composant résultants.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.

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
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

